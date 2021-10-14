---
title: Sevkiyat konsolidasyonu ilkeleri
description: Bu konu, sevkiyat konsolidasyon ilkelerinin esnek yapılandırmasını sağlayan işlevlere genel bir bakış sağlar.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationError, WHSShipConsolidationSetShipment, WHSShipConsolidationPolicySelect, WHSShipPlanningListPage, TMSCarrierGroup, WHSShipConsolidationTemplate, WHSShipConsolidationTemplateApply, WHSShipConsolidationTemplateCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 11ee4beefed02425d4650de3e896e608d3d00ef5
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577972"
---
# <a name="shipment-consolidation-policies"></a>Sevkiyat konsolidasyonu ilkeleri

[!include [banner](../includes/banner.md)]

Otomatik ve el ile gerçekleştirilen ambara serbest bırakma sırasında, sevkiyat konsolidasyon ilkelerini kullanan sevkiyat konsolidasyon süreci otomatik sevkiyat konsolidasyon işlemine olanak sağlar. Bu özelliğin öncesinde kullanılan otomatik konsolidasyon, sabit kodlanmış alanlar içeriyordu ve bir ambar için ayarlanmış olan **Ambara serbest bırakmada sevkiyatı konsolide et** alanına dayanıyordu.

Aşağıdaki işlevler için sevkiyat konsolidasyon ilkeleri kullanılır:

- Otomatik ambara serbest bırakma toplu işi
- Bir satış siparişi veya transfer emrindeki **Ambara serbest bırak** komutu
- Ayrılmış **Ambara serbest bırakma** sayfası
- **Yük planlama çalışma ekranı** sayfasında **Ambara serbest bırak** komutu
- **Sevkiyatları konsolide etme** ve **Sevkiyat konsolidasyonu çalışma ekranı** sayfalarında manuel sevkiyat konsolidasyonu

Sevkiyat konsolidasyonu ilkelerinin kullanılmaya başlanmasından önce, konsolidasyon işlevi ambar düzeyinde bir ayar olarak vardı. Tek bir ambardaki tüm müşterilerle ilgili tüm siparişler aynı konsolidasyon gereksinimlerine sahipmiş gibi işlenirdi. Sevkiyat konsolidasyon ilkeleri farklı kuruluşların farklı sevkiyat konsolidasyonu gereksinimlerine sahip olduğu senaryolar için destek sağlar.

Sorgular, uygulanan sevkiyat konsolidasyonu ilkesini tanımlamak için kullanılır ve daha sonra bir düzenlenebilir alanlar kümesi yükleme satırlarının sevkiyat düzeyinde nasıl gruplandığını belirler. (Bu model, dalga şablonlarının izleyeceği modele benzer.) Ayrıca, her ilkeye **Mevcut sevkiyatlarla konsolide et** seçeneği eklenmiştir. Bu seçenek etkinleştirildiğinde, *Ambara serbest bırakma* prosedürü, aynı konsolidasyon ilkesine göre oluşturulan mevcut sevkiyatlar arasında arama yaparak konsolidasyon için sevkiyatları bulur. Bu durumda, sistem yeni bir sevkiyat oluşturmak yerine, var olan bir sevkiyatı seçer veya yükler. Ancak, sistem yalnızca *Açık* durumundaki mevcut sevkiyatlar ile konsolide edilir; *Serbest bırakıldı* veya daha yüksek durumda olan bir dalga serbest bırakmasına ait olan sevkiyatlar konsolidasyon hedefleri olarak kabul edilmez.

Sevkiyat konsolidasyon ilkeleri kullanıma sunulduğunda, **Ambarlar** kurulum sayfasında daha önce var olan **Ambara serbest bırakmada sevkiyatı konsolide et** ayarı gizlenmiştir. Yeni sevkiyat konsolidasyonu özelliğine geçiş yapmanıza yardımcı olmak için **Sevkiyat konsolidasyon ilkeleri** sayfasındaki bir işlev, var olan ambarlara ait eski ayarı otomatik olarak içeren bir varsayılan ilke oluşturur. Bu varsayılan ilke oluşturulduktan sonra, **Ambarlar** kurulum sayfasındaki **Ambara serbest bırakmada sevkiyatı konsolide et** ayarı artık dikkate alınmaz.

İlgili konsolidasyon ilkesini, yerine getirme ilkelerini geçersiz kılabileceğiniz şekilde el ile geçersiz kılmak için **Ambara serbest bırak** sayfasını kullanabilirsiniz.

Ambara serbest bırakmadan önce, satış siparişi ve transfer emri satırlarına dayalı giden yükler oluşturmak için **Yük planlama çalışma ekranı** sayfasında **Serbest bırak \> Ambara serbest bırak** komutunu kullanabilirsiniz. Bu yüklemeler, sevkiyat ilkelerinin konsolidasyonu ile birlikte getirilen birleştirme mantığını kullanır.

Henüz onaylanmamış ancak ambara zaten serbest bırakılmış olan mevcut sevkiyatları konsolide etmek için **Sevkiyat konsolidasyonu çalışma ekranı** sayfasını kullanabilirsiniz. Bu işlevsellik, kendi sevkiyat konsolidasyonu olan otomatik serbest bırakma sürecinin günde birden çok kez çalıştırıldığı senaryoları destekler ancak, olası ek konsolidasyonlar, taşıyıcılara sevkiyat tamamlanmadan önce, onay işlemi sırasında manuel olarak tanımlanır. Bu işlevsellik, satış siparişi veya transfer emri satırlarından oluşturulan giden sevkiyatları, sevkiyatlar ambara serbest bırakıldıktan sonra ancak onaylanmadan önce istediğiniz zaman konsolide etmenize olanak sağlar.

**Sevkiyat konsolidasyonu çalışma ekranı** sayfası, birden çok sevkiyatı aynı anda değerlendirebildiğiniz ve konsolide edilmemiş bir siparişi belirli bir sevkiyata atayabildiğiniz, yük oluşturma çalışma ekranı gibi çalışır. Önerilen konsolidasyonları birden çok kez değerlendirmek ve onaylamak için sevkiyat konsolidasyonu şablonları uygulayabilirsiniz. Yetkisiz konsolidasyonları önlemek ve olası hatalarla ilgili olarak sizi uyarmak için bazı kurallar uygulanır.

## <a name="overview-of-new-functionality"></a>Yeni işlevlere genel bakış

Bu bölümde, *Sevkiyat konsolidasyon ilkeleri* özelliğini açıp kullandığınızda değiştirilen veya eklenen sayfalar, komutlar ve özellikler açıklanmıştır.

### <a name="shipment-consolidation-policies-page"></a>Sevkiyat konsolidasyon ilkeleri sayfası

İlkeler, iş emri türüne göre farklılaşır. **Satış siparişleri** türü, _Satış siparişi_ sevkiyatlarını ve **Transfer emri** türü, _Transfer çıkışı_ sevkiyatlarını temsil eder.

Her sevkiyat konsolidasyon ilkesinde, uygulandığı zamanı tanımlayan bir sorgu ve yürütme sırasını belirleyen bir sıra numarası vardır. Seçili alanların her bir benzersiz birleşimi için konsolidasyon uygulanır. Sağlanan ek bir parametre mevcut (açık) sevkiyatlarla konsolidasyon için kullanılır. İlkeler yeni sevkiyat oluşturulduğu her seferinde değerlendirilir ve uygulanır (dalga işlemeden önce).

Bir ilkede zorunlu alanlar eksikse veya yasak alanlar bulunuyorsa **Seçilen** bölümünde ilke, geçerli değil olarak işaretlenir. Zorunlu ve yasaklanmış alanların listeleri sabit kodlanmış ve genişletilebilir.

Aşağıdaki liste zorunlu alanları gösterir. Sevkiyatlar her zaman bu alanlara göre bölündüğünden, bu alanlar için farklı değerlere sahip birden çok sevkiyatı gruplayamazsınız.

- Satış siparişleri için:

    - **Hesap numarası:** _WHSShipmentTable.AccountNum_
    - **Teslimat alıcısı:** _WHSShipmentTable.DeliveryName_
    - **Posta adresi (RecId):** _WHSShipmentTable.DeliveryPostalAddress_
    - **Ambar:** _WHSShipmentTable.InventLocationId_

- Transfer emirleri için:

    - **Kaynak ambar:** _InventTransferTable.InventLocationIdFrom_
    - **Hedef ambar:** _InventTransferTable.InventLocationIdTo_

Aşağıdaki alanlar tüm belge türlerinde bulunmaz. Bu alanlar kullanıcı arabiriminde (UI) görünmez ve konsolidasyon için kullanılamaz.

- **Sevkiyat kodu:** _WHSShipmentTable.ShipmentId_
- **Durum:** _WHSShipmentTable.ShipmentStatus_
- **Sevkiyat konsolidasyon ilkesi:** _WHSShipmentTable.ShipConsolidationPolicyName_
- **İş hareketi türü:** _WHSShipmentTable.WorkTransType_
- **Dalga kodu:** _WHSShipmentTable.WaveId_
- **Yük kodu:** _WHSShipmentTable.LoadId_
- **Sevkiyat kodu:** _WHSLoadLine.ShipmentId_
- **Yük kodu:** _WHSLoadLine.LoadId_

Varsayılan olarak, bir ilke oluşturduğunuzda, zorunlu alanlar kümesi konsolidasyon alanları olarak kullanılır. Ancak, listede sol ok ve sağ ok düğmelerini kullanarak değişiklik yapabilirsiniz. (Bu işlem, dalga şablonlarında yöntemleri seçme işlemine benzer.)

Bu alanlar için kullanıcıların seçtiği değerler, yeni oluşturulan tüm sevkiyatlar için kullanılır veya bu sevkiyatlarla konsolidasyon sırasında var olan sevkiyatlara eklenir. İki sevkiyat, bu sevkiyatların konsolidasyonu için seçilen bir alanda aynı değere sahip olduğunda sevkiyatlar konsolide edilir. Aynı ilke, seçili olan sonraki tüm konsolidasyon alanları için geçerlidir. Değerler farklıysa ikinci sevkiyat iptal edilir ve yeni bir sevkiyat için seçilir. Otomatik konsolidasyon işlemi, sevkiyat konsolidasyon alanları için tüm benzersiz değer birleşimlerini oluşturduktan sonra ilgili birleşime bir sevkiyat atanmasını içerir.

Konsolidasyon işlemi sırasında seçilmemiş alanlar yoksayılır. İki sevkiyat seçilmemiş bir alan için farklı değerlere sahipse alan temizlenir (boş olarak ayarlanır). Her iki sevkiyat da seçilmemiş bir alan için aynı değere sahipse alan doldurulur.

Konsolidasyon alanlarının listesi (farklı değerlere sahip olduklarında temizlenecek alanlar) sabit kodlanır. Liste, yeni bir sevkiyat oluşturulduğunda satış siparişinden veya transfer emri satırından başlatılan tüm alanları içerir. Başka bir deyişle bir alan, satış siparişi veya transfer emri satırından başlatılmamışsa, var olan bir sevkiyata yeni veriler eklendiğinde yok sayılır.

### <a name="release-to-warehouse-page"></a>Ambara serbest bırakma sayfası

- Alt kılavuzdaki yeni bir alan, uygulanan konsolidasyon ilkesini gösterir.
- Yeni bir düğme, konsolidasyon ilkesini manuel olarak seçmenizi ve/veya geçersiz kılmanızı sağlar.

### <a name="release-to-warehouse-command-on-the-load-planning-workbench-page"></a>Yük planlama çalışma ekranı sayfasında Ambara serbest bırak komutu

- Mantık, uygulanan konsolidasyon ilkelerini kullanacak şekilde düzeltilmiştir.
- Sevkiyatlar artık yalnızca tek bir yük içinde konsolide edilir.

### <a name="consolidate-shipments-page"></a>Sevkiyatları konsolide etme sayfası

- Benzer sevkiyatlar (konsolidasyon adayları) için arama, sevkiyat konsolidasyon ilkesinde seçilen alanları kullanacak şekilde değiştirilmiştir.
- Farklı sevkiyatlarda farklı değerlere sahip alanlar artık boş olarak ayarlanır. (Daha önce, seçilen "taban" sevkiyattaki değerler kullanılıyordu.)

### <a name="shipment-consolidation-workbench-page"></a>Sevkiyat konsolidasyonu çalışma ekranı sayfası

- Yeni işlevler manuel konsolidasyon işlemini daha büyük bir ölçekte çoğaltır.
- Bu sayfayı artık **Ambar yönetimi** modülündeki **Ambara serbest bırak** menüsünden açabilirsiniz.
- Algoritma, henüz sevk edilmemiş var olan sevkiyatları analiz eder. Daha sonra konsolidasyon ilkelerinde seçilen alanları temel alarak konsolidasyon önerir.

## <a name="comparison-of-functionality"></a>İşlevsellik karşılaştırması

Aşağıdaki tablo, sevkiyat konsolidasyonu ilkelerini kullanmadığınız sırada ve bunları kullanırken sevkiyat konsolidasyonunun nasıl çalıştığını özetler.

| Sevkiyat konsolidasyon ilkeleri olmadan | Sevkiyat konsolidasyon ilkeleri ile |
|---|----|
| Geçerli değil | Konsolidasyon için seçilen satış veya transfer sevkiyatları, oluşturulan sevkiyatla aynı konsolidasyon ilkesine sahip olmalı veya açık bir sevkiyata (**Mevcut sevkiyatlarla konsolide et** seçeneği açık olduğunda) atanmalıdır. |
| *Ambara serbest bırakma* yordamı, konsolidasyon için bir sevkiyat bulmak amacıyla var olan sevkiyatlar arasında arama yapmaz. Yalnızca *Ambara serbest bırakma* yordamının geçerli bir örneği tarafından oluşturulan sevkiyatlar, konsolidasyon için bir sevkiyat bulmak amacıyla kullanılır. | **Mevcut sevkiyatlarla konsolide et** seçeneği kullanılmakta olan bir konsolidasyon ilkesi için açılırsa *Ambara serbest bırakma* yordamı, konsolidasyon için bir sevkiyat bulmak üzere aynı konsolidasyon ilkesine göre oluşturulmuş mevcut sevkiyatlar arasında arama yapar. Bu nedenle, iki ilkeniz varsa ilke 2'ye göre oluşturulan bir sevkiyat, ilke 1'e göre oluşturulan bir sevkiyatla hiçbir zaman konsolide edilmez. |
| Geçerli değil | Konsolidasyon ilkesi alanları listesi boşsa veya bir ilke bulunamazsa her satış siparişi veya transfer emri satırı için yeni bir sevkiyat oluşturulur. |
| Aşağıdaki konsolidasyon alanı, bir *transfer satırına* ait sevkiyatları konsolide etmek için kullanılan benzersiz değer birleşimini tanımlar. (Diğer tüm alanlar yok sayılır.)<ul><li>Sipariş numarası (OrderNum)</li></ul> | Aşağıdaki konsolidasyon alanları, bir *transfer satırına* ait sevkiyatları konsolide etmek için kullanılan benzersiz değer birleşimini tanımlar. (Diğer tüm alanlar yok sayılır.)<ul><li>Sipariş numarası (OrderNum)</li><li>Teslimat alıcısı (DeliveryName)</li><li>Posta adresi (DeliveryPostalAddress)</li><li>ISO ülke kodu (CountryRegionISOCode)</li><li>Adres (Address)</li><li>Tesis (InventSiteId)</li><li>Ambar (InventLocationId)</li><li>Sevkiyat taşıyıcısı (CarrierCode)</li><li>Taşıyıcı hizmeti (CarrierServiceCode)</li><li>Teslimat şekli (ModeCode)</li><li>Taşıyıcı grubu (CarrierGroupCode)</li><li>Teslimat koşulları (DlvTermId)</li></ul>Bu alanlar, yeni bir sevkiyat oluşturulduğunda mevcut ve başlatılmış olan tek alanlardır. |
| Aşağıdaki konsolidasyon alanları, bir *satış satırına* ait sevkiyatları konsolide etmek için kullanılan benzersiz değer birleşimini tanımlar. (Diğer tüm alanlar yok sayılır.)<ul><li>Sipariş numarası (OrderNum)</li><li>Müşteri referansı (CustomerRef)</li><li>Müşteri talebi (CustomerReq)</li><li>Teslimat koşulları (DlvTermId)</li></ul> | Aşağıdaki konsolidasyon alanları, bir *satış satırına* ait sevkiyatları konsolide etmek için kullanılan benzersiz değer birleşimini tanımlar. (Diğer tüm alanlar yok sayılır.)<ul><li>Sipariş numarası (OrderNum)</li><li>Hesap numarası (AccountNum)</li><li>Teslimat alıcısı (DeliveryName)</li><li>Posta adresi (DeliveryPostalAddress)</li><li>ISO ülke kodu (CountryRegionISOCode)</li><li>Adres (Address)</li><li>Tesis (InventSiteId)</li><li>Ambar (InventLocationId)</li><li>Sevkiyat taşıyıcısı (CarrierCode)</li><li>Taşıyıcı hizmeti (CarrierServiceCode)</li><li>Teslimat şekli (ModeCode)</li><li>Taşıyıcı grubu (CarrierGroupCode)</li><li>Aracı kodu (BrokerCode)</li><li>Yön (LoadDirection)</li><li>Teslimat koşulları (DlvTermId)</li><li>Müşteri referansı (CustomerRef)</li><li>Müşteri talebi (CustomerReq)</li></ul>Bu alanlar, yeni bir sevkiyat oluşturulduğunda mevcut ve başlatılmış olan tek alanlardır. |
| Geçerli değil | Aşağıdaki konsolidasyon alanları bir *satış satırı* için zorunludur ve kaldırılamaz:<ul><li>Hesap numarası (AccountNum)</li><li>Teslimat alıcısı (DeliveryName)</li><li>Posta adresi (DeliveryPostalAddress)</li><li>Ambar (InventLocationId)</li></ul>Varsayılan olarak, yeni bir ilke oluşturulduğunda bu alanlar atanacaktır. Bunlar kaldırılamaz. |
| **Yük planlama çalışma ekranı** sayfasında *Yükleri ambara serbest bırakma* yordamı, sevkiyatlar ve dalgalar oluşturmak için kendi ayrı kodunu kullanır. | Konsolidasyon için hangi alanların değerlendirilmesi gerektiğini belirlemek için sevkiyat konsolidasyon ilkeleri uygulanır. Sevkiyatlar yalnızca tek bir yük içinde konsolide edilir. |
| **Tüm sevkiyatlar** sayfasında **Sevkiyatları konsolide et** seçeneğini manuel olarak belirlersiniz ve sonra bir hedef "taban" sevkiyat seçersiniz. Filtre, bazı temel alanlar için eşleşen değerlere sahip var olan tüm sevkiyatları önerir. | **Tüm sevkiyatlar** sayfasında **Sevkiyatları konsolide et** seçeneğini manuel olarak belirlersiniz ve sonra bir hedef "taban" sevkiyat seçersiniz. Sistem, ilgili sevkiyat konsolidasyon ilkeleri için yapılandırılan çeşitli temel alanların değerlerini eşleştirerek, var olan başka sevkiyatları önerir. |
| **Tüm sevkiyatlar** sayfasında **Sevkiyatları konsolide et** komutunu yalnızca tek bir sevkiyat için kullanabilirsiniz. | **Sevkiyat konsolidasyonu çalışma ekranı** sayfası, henüz sevk edilmiş durumda olmayan bir sevkiyat kümesini bulmanıza yardımcı olur. Bu sevkiyatlar, sevkiyat konsolidasyon ilkelerinizde yapılandırılan çeşitli temel alanlara göre analiz edilir. Bu alanların değerlerinin eşleştiği sevkiyatlar konsolidasyon için tavsiye edilir.<p>Önerilen konsolidasyonlardan sevkiyatları kaldırarak ve/veya bunlara sevkiyatlar ekleyerek konsolidasyona manuel bakım yapabilirsiniz. Çeşitli türlerde hatalar oluşabilir ancak bunların bazılarını geçersiz kılabilirsiniz.</p> |
| **Tasarım notu:** *Satış siparişlerini ambara otomatik serbest bırakma* yordamı, satış satırlarını gruplar halinde böler. Her grup kendi benzersiz **ReleaseToWarehouseId** değerine sahiptir ve *Ambara serbest bırakma* yordamına göre ayrı olarak işlenir. Bu yordam, iş kesme kurulumuna bakılmaksızın yeni iş oluşturur. | **Tasarım notu:** *Satış siparişlerini ambara otomatik serbest bırakma* yordamı, işlenmekte olan tüm satış satırlarına aynı **ReleaseToWarehouseId** değerini atar. Tüm satış satırları aynı anda *Ambara serbest bırakma* yordamı tarafından aynı anda işlenir. Önceki davranışı sağlamak için her sevkiyat kodu için iş sonunu yapılandırmanız gerekir. |

## <a name="additional-resources"></a>Ek kaynaklar

- [Sevkiyat konsolidasyon ilkelerini yapılandırma](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
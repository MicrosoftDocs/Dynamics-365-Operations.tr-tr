---
title: Mağazalardaki müşteri yönetimi
description: Bu konu, perakendecilerin müşteri yönetimi yeteneklerini Microsoft Dynamics 365 Commerce'teki satış noktasında nasıl etkinleştirebileceğini açıklar.
author: josaw1
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 46a18d36a389e8a52253c2c3a153e0eae95c0e57
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799433"
---
# <a name="customer-management-in-stores"></a>Mağazalardaki müşteri yönetimi

[!include [banner](includes/banner.md)]

Bu konu, perakendecilerin müşteri yönetimi yeteneklerini Microsoft Dynamics 365 Commerce'teki satış noktasında nasıl etkinleştirebileceğini açıklar.

Mağaza görevlilerinin, POS'ta müşteri kayıtlarını oluşturabilmesi ve düzenleyebilmesi önemlidir. Bu şekilde, e-posta adresi, telefon numarası ve adres gibi müşteri bilgileri ile ilgili güncelleştirmeleri kaydedebilirler. Bu bilgiler pazarlama gibi aşağı akış yönündeki sistemlerde yararlıdır, çünkü bu sistemlerin verimliliği müşteri verilerinin doğruluğuna bağlıdır.

Satış yetkilileri, müşteri oluşturma iş akışını iki POS giriş noktasından tetikleyebilir. **Müşteri ekleme** işlemiyle eşlenen bir düğme seçebilir veya Arama sonuçları sayfasında uygulama çubuğunda **müşteri oluştur**'u seçebilirler. Her iki durumda da, Satış yetkililerinin müşteri adı, e-posta adresi, telefon numarası, adres ve işle ilgili tüm ek bilgiler gibi gerekli müşteri ayrıntılarını girebileceği **yeni müşteri** iletişim kutusu görüntülenir. Ek bilgiler müşteriyle ilişkili müşteri öznitelikleri kullanılarak kaydedilebilir. Müşteri öznitelikleri hakkında daha fazla bilgi için [Müşteri özniteliklerine](dev-itpro/customer-attributes.md) bakın.

Satış yetkilileri ikincil e-posta adreslerini ve telefon numaralarını da kaydedebilir. Ek olarak, müşterilerin, bu ikincil e-posta adreslerinden veya telefon numaralarından herhangi biriyle pazarlama bilgilerini alma tercihini kaydedebilirler. Bu yeteneği etkinleştirmek için, perakendeciler, Commerce genel merkezindeki **özellik yönetimi** çalışma alanında bulunan **Pazarlama için bu kişilerin birden fazla e-posta adresini, telefon numarasını ve onayını kaydet** (**Sistem Yönetimi \> çalışma alanları \>Özellik Yönetimi**) özelliğini etkinleştirmelidir.

## <a name="default-customer-properties"></a>Varsayılan müşteri özellikleri

Perakendeciler, her mağaza için varsayılan bir müşteri ilişkilendirmek amacıyla Commerce genel merkezindeki (**perakende ve Commerce \> Kanallar \> Mağazalar**) **tüm mağazalar** sayfasını kullanabilir. Böylece Commerce, varsayılan müşteri için tanımlanan özellikleri, oluşturulan tüm yeni müşteri kayıtlarına kopyalar. Örneğin, **Müşteri Oluştur** iletişim kutusu, mağazayla ilişkilendirilmiş olan varsayılan müşteriden alınan özellikleri gösterir. Bu özellikler müşteri türü, müşteri grubu, makbuz tercihi, para birimi ve dili içerir. Tüm ilişkiler de (müşteri grupları) varsayılan müşteriden devralınır. Ancak, mali boyutlar varsayılan müşterinin kendisinden değil, varsayılan müşteriyle ilişkilendirilmiş müşteri grubundan devralınır.

Satış yetkilileri bir müşteri için birden fazla adres kaydedebilir. Müşterinin adı ve telefon numarası, her bir adresle ilişkilendirilmiş iletişim bilgilerinden devralınır. Müşteri kaydının **adresler** hızlı sekmesi, satış yetkilisinin düzenleyebileceği bir **amaç** alanı içerir. Müşteri türü **kişi** ise , varsayılan değer **ev** olur. Müşteri türü **Kuruluş** ise , varsayılan değer **İş** olur. Bu alanın desteklediği diğer değerler **Ev**, **ofis** ve **posta kutusu**'nu içerir. Bir adresin **ülke** alanının değeri, **kuruluş yönetimi \> Kuruluşlar \> işletim birimleri** içindeki Commerce genel merkezinde bulunan **işletim birimi** sayfasında belirtilen birincil adresten devralınır.

## <a name="sync-customers-and-async-customers"></a>Zaman uyumlu müşteriler ve zaman uyumsuz müşteriler

Commerce'te, iki müşteri oluşturma modu vardır: Zaman uyumlu (veya Eşitleme) ve zaman uyumsuz (veya asenkron). Varsayılan olarak, müşteriler zaman uyumlu olarak oluşturulur. Başka bir deyişle, bunlar Commerce genel merkezinde gerçek zamanlı olarak oluşturulur. Zaman uyumlu müşteri oluşturma modu, tüm kanallar arasında yeni müşteriler hemen aranabilir hale geldiği için yararlıdır. Ancak, bir dezavantajı da vardır. Commerce genel merkezine [Commerce Data Exchange: Gerçek Zamanlı Servis](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) çağrıları oluşturduğundan, birçok eşzamanlı müşteri oluşturma çağrısı yapılırsa performans etkilenebilir.

**Zaman uyumsuz modda müşteri oluştur** seçeneği mağazanın işlevsellik profilinde **Evet** olarak ayarlanmışsa (**Perakende ve Commerce \> Channel kurulum \> çevrimiçi mağaza kurulumu \> İşlev profilleri**), gerçek zamanlı Servis çağrıları kanal veritabanında müşteri kayıtları oluşturmak için kullanılmaz. Zaman uyumsuz müşteri oluşturma modu, Commerce genel merkezinin performansını etkilemez. Bir geçici genel benzersiz tanımlayıcı (GUID), her yeni zaman uyumsuz müşteri kaydına atanır ve müşteri hesap kodu olarak kullanılır. Bu GUID, POS kullanıcıları için gösterilmez. Bunun yerine, bu kullanıcılar müşteri hesap kodu olarak **bekleyen eşitlemeyi** görürler. Bu yapılandırma müşterilerinin zaman uyumsuz olarak oluşturulmasını zorsa da, müşteri kayıtlarına yapılan düzenlemelerin her zaman zaman uyumlu olarak yapılacağını unutmayın.

### <a name="convert-async-customers-to-sync-customers"></a>Zaman uyumsuz müşterileri zaman uyumlu müşterilere dönüştürme

Zaman uyumsuz müşterileri zaman uyumlu müşterilere dönüştürmek için, önce zaman uyumsuz müşterileri Commerce genel merkezine göndermek üzere P-job'ı çalıştırmanız gerekir. Sonra Müşteri hesap kodları oluşturmak için **müşterileri ve iş ortaklarını zaman uyumsuz modda Eşitle** işini çalıştırın. Son olarak, yeni müşteri hesap kodlarını kanallarla eşitlemek için **1010** işini çalıştırın.

### <a name="async-customer-limitations"></a>Zaman uyumsuz müşteri sınırlamaları

Zaman uyumsuz müşteri işlevinde şu sınırlamalar vardır:

- Müşteri Commerce genel merkezinde oluşturulmadıysa ve yeni müşteri hesap kodu kanala geri eşitlenmediyse zaman uyumsuz müşteri kayıtları düzenlenemez.
- İlişkiler zaman uyumsuz müşterilerle ilişkilendirilemez. Bu nedenle, yeni zaman uyumsuz müşteriler ilişkileri varsayılan müşteriden devralmaz.
- Yeni müşteri hesap kodu kanalla geri eşitlenmedikçe, bağlılık programı kartları zaman uyumsuz müşterilere verilemez.
- Zaman uyumsuz müşteriler ikincil e-posta adresleri ve telefon numaraları kaydedilemez.

### <a name="customer-creation-in-pos-offline-mode"></a>POS Çevrimdışı modunda müşteri oluşturma

Zaman uyumsuz müşteri oluşturma modu etkinken POS'un çevrimdışı olması durumunda, yeni müşteri kayıtları zaman uyumsuz olarak oluşturulur. Zaman uyumsuz müşteri oluşturma modu devre dışıyken POS'un çevrimdışı olması durumunda, sistem otomatik olarak zaman uyumsuz müşteri oluşturma moduna geçer. Başka bir deyişle, zaman uyumsuz müşteri oluşturma modu devre dışı olsa bile müşteri kayıtları zaman uyumsuz olarak oluşturulabilir. Bu nedenle, Commerce genel merkezi yöneticilerinin zaman uyumsuz müşterilerin Commerce genel merkezinde zaman uyumlu müşterilere dönüştürülmesi için P-job, **Zaman uyumsuz modundan müşteri ve iş ortaklarını Eşitle** işi ve **1010** işi için yinelenen bir toplu iş oluşturup planlaması gerekir.

> [!NOTE]
> **Paylaşılan müşteri veri tablolarını filtrele** seçeneği, **Commerce kanal şeması** sayfasında **Evet** olarak ayarlanmışsa (**Perakende ve Commerce \> Genel merkez kurulumu \> Commerce Planlayıcı \> Kanal veritabanı grubu**), müşteri kayıtları POS çevrimdışı modunda oluşturulmaz. Daha fazla bilgi için bkz. [Çevrimdışı veri hariç tutma](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Ek kaynaklar

[Müşteri öznitelikleri](dev-itpro/customer-attributes.md)

[Çevrimdışı veri hariç tutma](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)

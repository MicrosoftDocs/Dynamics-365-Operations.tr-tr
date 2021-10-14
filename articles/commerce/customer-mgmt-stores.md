---
title: Mağazalardaki müşteri yönetimi
description: Bu konu, perakendecilerin müşteri yönetimi yeteneklerini Microsoft Dynamics 365 Commerce'teki satış noktasında nasıl etkinleştirebileceğini açıklar.
author: josaw1
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4fd6039843be09ec706e45746d5724faa99a95e6
ms.sourcegitcommit: 3f59b15ba7b4c3050f95f2b32f5ae6d7b96e1392
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/29/2021
ms.locfileid: "7563073"
---
# <a name="customer-management-in-stores"></a>Mağazalardaki müşteri yönetimi

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Bu konu, perakendecilerin müşteri yönetimi yeteneklerini Microsoft Dynamics 365 Commerce'teki satış noktasında nasıl etkinleştirebileceğini açıklar.

Mağaza görevlilerinin, POS'ta müşteri kayıtlarını oluşturabilmesi ve düzenleyebilmesi önemlidir. Bu şekilde, e-posta adresi, telefon numarası ve adres gibi müşteri bilgileri ile ilgili güncelleştirmeleri kaydedebilirler. Bu bilgiler pazarlama gibi aşağı akış yönündeki sistemlerde yararlıdır, çünkü bu sistemlerin verimliliği müşteri verilerinin doğruluğuna bağlıdır.

Satış yetkilileri, müşteri oluşturma iş akışını iki POS giriş noktasından tetikleyebilir. **Müşteri ekleme** işlemiyle eşlenen bir düğme seçebilir veya Arama sonuçları sayfasında uygulama çubuğunda **müşteri oluştur**'u seçebilirler. Her iki durumda da, Satış yetkililerinin müşteri adı, e-posta adresi, telefon numarası, adres ve işle ilgili tüm ek bilgiler gibi gerekli müşteri ayrıntılarını girebileceği **yeni müşteri** iletişim kutusu görüntülenir. Ek bilgiler müşteriyle ilişkili müşteri öznitelikleri kullanılarak kaydedilebilir. Müşteri öznitelikleri hakkında daha fazla bilgi için [Müşteri özniteliklerine](dev-itpro/customer-attributes.md) bakın.

Satış yetkilileri ikincil e-posta adreslerini ve telefon numaralarını da kaydedebilir. Ek olarak, müşterilerin, bu ikincil e-posta adreslerinden veya telefon numaralarından herhangi biriyle pazarlama bilgilerini alma tercihini kaydedebilirler. Bu yeteneği etkinleştirmek için, perakendeciler, Commerce genel merkezindeki **özellik yönetimi** çalışma alanında bulunan **Pazarlama için bu kişilerin birden fazla e-posta adresini, telefon numarasını ve onayını kaydet** (**Sistem Yönetimi \> çalışma alanları \>Özellik Yönetimi**) özelliğini etkinleştirmelidir.

## <a name="default-customer-properties"></a>Varsayılan müşteri özellikleri

Perakendeciler, her mağaza için varsayılan bir müşteri ilişkilendirmek amacıyla Commerce genel merkezindeki (**perakende ve Commerce \> Kanallar \> Mağazalar**) **tüm mağazalar** sayfasını kullanabilir. Böylece Commerce, varsayılan müşteri için tanımlanan özellikleri, oluşturulan tüm yeni müşteri kayıtlarına kopyalar. Örneğin, **Müşteri Oluştur** iletişim kutusu, mağazayla ilişkilendirilmiş olan varsayılan müşteriden alınan özellikleri gösterir. Bu özellikler **müşteri türü**, **müşteri grubu**, **makbuz seçeneği**, **makbu e-postası**, **para birimi** ve **dili** içerir. Tüm **ilişkiler** de (müşteri grupları) varsayılan müşteriden devralınır. Ancak, **mali boyutlar** varsayılan müşterinin kendisinden değil, varsayılan müşteriyle ilişkilendirilmiş müşteri grubundan devralınır.

> [!NOTE]
> **Makbuz e-postası** değeri, yalnızca yeni oluşturulan müşteriler için makbuz e-posta kimliği sağlanmadıysa varsayılan müşteriden kopyalanır. Bu, makbuz e-posta kimliği varsayılan müşteride varsa, e-ticaret sitesinden oluşturulan tüm müşterilerin, müşteriden gelen makbuz e-posta kimliğini yakalamak için kullanıcı arabirimi olmadığı için aynı makbuz e-posta kimliğini alacağı anlamına gelir. **Makbuz e-postası** alanını mağazanın varsayılan müşterisi için boş bırakmanızı ve yalnızca mevcut bir makbuz e-postası adresine bağlı bir iş süreciniz varsa kullanmanızı öneririz. 

Satış yetkilileri bir müşteri için birden fazla adres kaydedebilir. Müşterinin adı ve telefon numarası, her bir adresle ilişkilendirilmiş iletişim bilgilerinden devralınır. Müşteri kaydının **adresler** hızlı sekmesi, satış yetkilisinin düzenleyebileceği bir **amaç** alanı içerir. Müşteri türü **kişi** ise , varsayılan değer **ev** olur. Müşteri türü **Kuruluş** ise , varsayılan değer **İş** olur. Bu alanın desteklediği diğer değerler **Ev**, **ofis** ve **posta kutusu**'nu içerir. Bir adresin **ülke** alanının değeri, **kuruluş yönetimi \> Kuruluşlar \> işletim birimleri** içindeki Commerce genel merkezinde bulunan **işletim birimi** sayfasında belirtilen birincil adresten devralınır.

## <a name="sync-customers-and-async-customers"></a>Zaman uyumlu müşteriler ve zaman uyumsuz müşteriler

> [!IMPORTANT]
> POS çevrimdışı olduğunda Zaman Uyumsuz müşteri oluşturma modu devre dışı bırakılsa bile sistem otomatik olarak müşterileri zaman uyumsuz olarak oluşturur. Bu nedenle, Zaman Uyumlu ve Zaman Uyumsuz müşteri oluşturma modları arasındaki seçiminiz ne olursa olsun Commerce genel merkezi yöneticilerinin **P işi**, **Müşterileri ve iş ortaklarını zaman uyumsuz moddan eşitle** işi (eski adıyla **Müşterileri ve iş ortaklarını zaman uyumsuz moddan eşitle** işi) ve **1010** işi için yinelenen bir toplu iş oluşturması ve zamanlaması gerekir. Böylece tüm Zaman Uyumsuz müşteriler Commerce genel merkezindeki Zaman Uyumlu müşterilere dönüştürülür.

Commerce'te, iki müşteri oluşturma modu vardır: Zaman uyumlu (veya Eşitleme) ve zaman uyumsuz (veya asenkron). Varsayılan olarak, müşteriler zaman uyumlu olarak oluşturulur. Başka bir deyişle, bunlar Commerce genel merkezinde gerçek zamanlı olarak oluşturulur. Zaman uyumlu müşteri oluşturma modu, tüm kanallar arasında yeni müşteriler hemen aranabilir hale geldiği için yararlıdır. Ancak, bir dezavantajı da vardır. Commerce genel merkezine [Commerce Data Exchange: Gerçek Zamanlı Servis](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) çağrıları oluşturduğundan, birçok eşzamanlı müşteri oluşturma çağrısı yapılırsa performans etkilenebilir.

**Zaman uyumsuz modda müşteri oluştur** seçeneği mağazanın işlevsellik profilinde **Evet** olarak ayarlanmışsa (**Perakende ve Commerce \> Channel kurulum \> çevrimiçi mağaza kurulumu \> İşlev profilleri**), gerçek zamanlı Servis çağrıları kanal veritabanında müşteri kayıtları oluşturmak için kullanılmaz. Zaman uyumsuz müşteri oluşturma modu, Commerce genel merkezinin performansını etkilemez. Bir geçici genel benzersiz tanımlayıcı (GUID), her yeni zaman uyumsuz müşteri kaydına atanır ve müşteri hesap kodu olarak kullanılır. Bu GUID, POS kullanıcıları için gösterilmez. Bunun yerine, bu kullanıcılar müşteri hesap kodu olarak **bekleyen eşitlemeyi** görürler. 

### <a name="convert-async-customers-to-sync-customers"></a>Zaman uyumsuz müşterileri zaman uyumlu müşterilere dönüştürme

Zaman Uyumsuz müşterileri Zaman Uyumlu müşterilere dönüştürmek için öncelikle Zaman Uyumsuz müşterileri Commerce genel merkezine göndermek üzere **P işi**'ni çalıştırmanız gerekir. Ardından, müşteri hesap kodları oluşturmak için **Müşterileri ve iş ortaklarını zaman uyumsuz moddan eşitle** işini (eski adıyla **Müşterileri ve iş ortaklarını zaman uyumsuz moddan eşitle**) çalıştırın. Son olarak, yeni müşteri hesap kodlarını kanallarla eşitlemek için **1010** işini çalıştırın.

### <a name="async-customer-limitations"></a>Zaman uyumsuz müşteri sınırlamaları

Zaman uyumsuz müşteri işlevinde şu sınırlamalar vardır:

- Müşteri Commerce genel merkezinde oluşturulmadıysa ve yeni müşteri hesap kodu kanala geri eşitlenmediyse zaman uyumsuz müşteri kayıtları düzenlenemez. Bu nedenle, bir müşteri adresinin eklenmesi müşteri profili üzerinde bir düzenleme işlemi şeklinde dahili olarak uygulandığından bir Zaman Uyumsuz müşteri için adres, o müşteri Commerce genel merkeziyle eşitlenene kadar kaydedilemez. Ancak **Müşteri adresleri için zaman uyumsuz oluşturmayı etkinleştir** özelliği etkinleştirilirse Zaman Uyumsuz müşteriler için müşteri adresleri de kaydedilebilir.
- İlişkiler zaman uyumsuz müşterilerle ilişkilendirilemez. Bu nedenle, yeni zaman uyumsuz müşteriler ilişkileri varsayılan müşteriden devralmaz.
- Yeni müşteri hesap kodu kanalla geri eşitlenmedikçe, bağlılık programı kartları zaman uyumsuz müşterilere verilemez.
- Zaman uyumsuz müşteriler ikincil e-posta adresleri ve telefon numaraları kaydedilemez.

Daha önce bahsedilen sınırlamalardan bazıları, işletmeniz için Zaman Uyumlu müşteri seçeneğini tercih etmenize neden olsa da Commerce ekibi, Zaman Uyumsuz müşteri özelliklerini Zaman Uyumlu müşteri özellikleriyle daha yakından eşleştirmek için çalışmaktadır. Örneğin, Commerce uygulamasının 10.0.22 sürümünden itibaren **Özellik yönetimi** çalışma alanında etkinleştirebileceğiniz yeni bir **Müşteri adresleri için zaman uyumsuz oluşturmayı etkinleştir** özelliği, hem Zaman Uyumlu müşteriler hem de Zaman Uyumsuz müşteriler için yeni oluşturulan müşteri adreslerini kaydeder. Bu adresleri Commerce genel merkezindeki müşteri profiline kaydetmek için **P işi**, **Müşterileri ve iş ortaklarını zaman uyumsuz moddan eşitle** işi ve **1010** işi için yinelenen bir toplu iş zamanlamanız gerekir. Böylece tüm Zaman Uyumsuz müşteriler Commerce genel merkezindeki Zaman Uyumlu müşterilere dönüştürülür.

### <a name="customer-creation-in-pos-offline-mode"></a>POS Çevrimdışı modunda müşteri oluşturma

POS çevrimdışı olduğunda Zaman Uyumsuz müşteri oluşturma modu devre dışı bırakılsa bile sistem otomatik olarak müşterileri zaman uyumsuz olarak oluşturur. Bu nedenle, daha önce de belirtildiği gibi Commerce genel merkezi yöneticilerinin Zaman Uyumsuz müşterilerin Commerce genel merkezinde Zaman Uyumlu müşterilere dönüştürülmesi için **P işi**, **Müşterileri ve iş ortaklarını zaman uyumsuz moddan eşitle** işi ve **1010** işi için yinelenen bir toplu iş oluşturup zamanlaması gerekir.

> [!NOTE]
> **Paylaşılan müşteri veri tablolarını filtrele** seçeneği, **Commerce kanal şeması** sayfasında **Evet** olarak ayarlanmışsa (**Perakende ve Commerce \> Genel merkez kurulumu \> Commerce Planlayıcı \> Kanal veritabanı grubu**), müşteri kayıtları POS çevrimdışı modunda oluşturulmaz. Daha fazla bilgi için bkz. [Çevrimdışı veri hariç tutma](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Ek kaynaklar

[Müşteri öznitelikleri](dev-itpro/customer-attributes.md)

[Çevrimdışı veri hariç tutma](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)

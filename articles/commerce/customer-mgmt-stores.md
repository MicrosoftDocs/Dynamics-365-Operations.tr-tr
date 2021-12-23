---
title: Mağazalardaki müşteri yönetimi
description: Bu konu, perakendecilerin müşteri yönetimi yeteneklerini Microsoft Dynamics 365 Commerce'teki satış noktasında nasıl etkinleştirebileceğini açıklar.
author: gvrmohanreddy
ms.date: 12/10/2021
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
ms.openlocfilehash: 29e45419f712e25092b473e34144ac1146e4ed9b
ms.sourcegitcommit: eef5d9935ccd1e20e69a1d5b773956aeba4a46bc
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/11/2021
ms.locfileid: "7913638"
---
# <a name="customer-management-in-stores"></a>Mağazalardaki müşteri yönetimi

[!include [banner](includes/banner.md)]

Bu konu, perakendecilerin müşteri yönetimi yeteneklerini Microsoft Dynamics 365 Commerce'teki satış noktasında nasıl etkinleştirebileceğini açıklar.

Mağaza görevlilerinin, POS'ta müşteri kayıtlarını oluşturabilmesi ve düzenleyebilmesi önemlidir. Bu şekilde, e-posta adresi, telefon numarası ve adres gibi müşteri bilgileri ile ilgili güncelleştirmeleri kaydedebilirler. Bu bilgiler pazarlama gibi aşağı akış yönündeki sistemlerde yararlıdır, çünkü bu sistemlerin verimliliği müşteri verilerinin doğruluğuna bağlıdır.

Satış yetkilileri, müşteri oluşturma iş akışını iki POS giriş noktasından tetikleyebilir. **Müşteri ekleme** işlemiyle eşlenen bir düğme seçebilir veya Arama sonuçları sayfasında uygulama çubuğunda **müşteri oluştur**'u seçebilirler. Her iki durumda da, Satış yetkililerinin müşteri adı, e-posta adresi, telefon numarası, adres ve işle ilgili tüm ek bilgiler gibi gerekli müşteri ayrıntılarını girebileceği **yeni müşteri** iletişim kutusu görüntülenir. Ek bilgiler müşteriyle ilişkili müşteri öznitelikleri kullanılarak kaydedilebilir. Müşteri öznitelikleri hakkında daha fazla bilgi için [Müşteri özniteliklerine](dev-itpro/customer-attributes.md) bakın.

Satış yetkilileri ikincil e-posta adreslerini ve telefon numaralarını da kaydedebilir. Ek olarak, müşterilerin, bu ikincil e-posta adreslerinden veya telefon numaralarından herhangi biriyle pazarlama bilgilerini alma tercihini kaydedebilirler. Bu yeteneği etkinleştirmek için, perakendeciler, Commerce genel merkezindeki **özellik yönetimi** çalışma alanında bulunan **Pazarlama için bu kişilerin birden fazla e-posta adresini, telefon numarasını ve onayını kaydet** (**Sistem Yönetimi \> çalışma alanları \>Özellik Yönetimi**) özelliğini etkinleştirmelidir.

## <a name="default-customer-properties"></a>Varsayılan müşteri özellikleri

Perakendeciler, her mağaza için varsayılan bir müşteri ilişkilendirmek amacıyla Commerce genel merkezindeki (**perakende ve Commerce \> Kanallar \> Mağazalar**) **tüm mağazalar** sayfasını kullanabilir. Böylece Commerce, varsayılan müşteri için tanımlanan özellikleri, oluşturulan tüm yeni müşteri kayıtlarına kopyalar. Örneğin, **Müşteri Oluştur** iletişim kutusu, mağazayla ilişkilendirilmiş olan varsayılan müşteriden alınan özellikleri gösterir. Bu özellikler **müşteri türü**, **müşteri grubu**, **makbuz seçeneği**, **makbu e-postası**, **para birimi** ve **dili** içerir. Tüm **ilişkiler** de (müşteri grupları) varsayılan müşteriden devralınır. Ancak, **mali boyutlar** varsayılan müşterinin kendisinden değil, varsayılan müşteriyle ilişkilendirilmiş müşteri grubundan devralınır.

> [!NOTE]
> **Makbuz e-postası** değeri, yalnızca yeni oluşturulan müşteriler için makbuz e-posta kimliği sağlanmadıysa varsayılan müşteriden kopyalanır. Bu, makbuz e-posta kimliği varsayılan müşteride varsa, e-ticaret sitesinden oluşturulan tüm müşterilerin, müşteriden gelen makbuz e-posta kimliğini yakalamak için kullanıcı arabirimi olmadığı için aynı makbuz e-posta kimliğini alacağı anlamına gelir. **Makbuz e-postası** alanını mağazanın varsayılan müşterisi için boş bırakmanızı ve yalnızca mevcut bir makbuz e-postası adresine bağlı bir iş süreciniz varsa kullanmanızı öneririz. 

Satış yetkilileri bir müşteri için birden fazla adres kaydedebilir. Müşterinin adı ve telefon numarası, her bir adresle ilişkilendirilmiş iletişim bilgilerinden devralınır. Müşteri kaydının **adresler** hızlı sekmesi, satış yetkilisinin düzenleyebileceği bir **amaç** alanı içerir. Müşteri türü **kişi** ise , varsayılan değer **ev** olur. Müşteri türü **Kuruluş** ise , varsayılan değer **İş** olur. Bu alanın desteklediği diğer değerler **Ev**, **ofis** ve **posta kutusu**'nu içerir. Bir adresin **ülke** alanının değeri, **kuruluş yönetimi \> Kuruluşlar \> işletim birimleri** içindeki Commerce genel merkezinde bulunan **işletim birimi** sayfasında belirtilen birincil adresten devralınır.



## <a name="additional-resources"></a>Ek kaynaklar

[Zaman uyumsuz müşteri oluşturma modu](async-customer-mode.md)

[Zaman uyumsuz müşterileri zaman uyumlu müşterilere dönüştürme](convert-async-to-sync.md)

[Müşteri öznitelikleri](dev-itpro/customer-attributes.md)

[Çevrimdışı veri hariç tutma](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)

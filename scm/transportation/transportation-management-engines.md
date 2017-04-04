---
title: "Taşıma yönetimi altyapıları"
description: "Nakliye yönetimi motorları, Nakliye yönetimindeki nakliye oranlarının oluşturulması ve işlenmesi için kullanılan mantığı tanımlar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TMSFreightBillType, TMSGenericEngine, TMSMileageEngine, TMSRateEngine, TMSTransitTimeEngine, TMSZoneEngine
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12234
ms.assetid: b878478c-0e04-4a1e-a037-6fdbb345a9a3
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 9db73514d71239d75dc63fcf6e9f45923b1272f4
ms.lasthandoff: 03/31/2017


---

# <a name="transportation-management-engines"></a>Taşıma yönetimi altyapıları

Nakliye yönetimi motorları, Nakliye yönetimindeki nakliye oranlarının oluşturulması ve işlenmesi için kullanılan mantığı tanımlar. 

Bir taşıma yönetimi altyapısı, taşıyıcının ulaşım hızı gibi görevleri hesaplar. Altyapı sistemi, Microsoft Dynamics 365 for Operations verilerini temel alarak hesaplama stratejilerini çalışma zamanında değiştirmenize olanak tanır. Taşıma yönetimi altyapısı, belirli bir taşıyıcı sözleşmesiyle ilişkili bir eklentiye benzer.

## <a name="what-engines-are-available"></a>Hangi altyapılar var?
Aşağıdaki tablo, Microsoft Dynamics 365 for Operations uygulamasında kullanılabilen taşıma yönetimi altyapılarını gösterir.

| Taşıma yönetimi altyapısı | Açıklama                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Değerlendirme altyapısı**                  | Oranları hesaplar.                                                                                                                                                                                                                                                                                                           |
| **Genel altyapı**               | Microsoft Dynamics 365 for Operations'dan veri istemeyen diğer altyapılar tarafından kullanılan basit yedek altyapılar, örneğin bir paylaştırma altyapısı. Paylaştırma altyapıları, belirli siparişlere ve satırlara taşımanın nihai maliyetlerini, hacim ve ağırlık gibi boyutlara dayalı olarak azaltmak için kullanılır. |
| **Mesafe altyapısı**               | Taşıma mesafesini hesaplar.                                                                                                                                                                                                                                                                                     |
| **Yoldaki süre altyapısı**          | Başlangıçtan son hedefe seyahat için gereken süreyi hesaplar.                                                                                                                                                                                                                                       |
| **Bölge altyapısı**                  | Geçerli adrese dayalı olarak bölgeyi hesaplar ve A adresinden B adresine gitmek için geçilmesi gereken bölge sayısını hesaplar.                                                                                                                                                                    |
| **Navlun fatura türü**            | Navlun faturasını ve navlun faturası satırlarını standartlaştırır ve otomatik navlun faturası eşleştirmesi için kullanılır.                                                                                                                                                                                                                |

 
<a name="what-engines-must-be-configured-to-rate-a-shipment"></a>Bir sevkıyatı değerlendirmek için hangi altyapılar yapılandırılmalıdır?
---------------------------------------------------

Bir sevkıyatı belirli bir taşıyıcı kullanarak değerlendirmek için, birden fazla taşıma yönetimi altyapısı yapılandırmanız gerekir. **Değerlendirme altyapısı** gereklidir, ancak **Değerlendirme altyapısı**'nı desteklemek için diğer taşıma yönetimi altyapıları gerekebilir. Örneğin, **Değerlendirme altyapısı**, değerlendirmeyi kaynak ile hedef arasındaki mesafeye dayalı olarak hesaplamak için **Mesafe altyapısı**'ndan veri almak için kullanılabilir.

## <a name="whats-required-to-initialize-a-transportation-management-engine"></a>Bir taşıma yönetimi altyapısını başlatmak için ne gerekir?
Taşıma yönetimi altyapısı, belirli bir şekilde işlemesi için başlangıç verileri ayarlamanızı gerektirir. Kurulum aşağıdaki veri türlerini içerebilir:
-   Diğer taşıma yönetimi altyapılarına başvurur. Ayrıntılar için, bu bölümdeki yapılandırma örneğine bakın.
-   Taşıma yönetimi altyapısı tarafından kullanılan .NET türlerine başvurur.
-   Basit yapılandırma verileri.

Birçok durumda, taşıma yönetimi altyapısının kurulum formlarındaki **Parametreler** düğmesine tıklayarak başlangıç verilerini yapılandırabilirsiniz. **Bir mesafe altyapısına başvuran bir değerlendirme altyapısının yapılandırılmasına dair örnek** Aşağıdaki örnekte, .NET altyapısı türü Microsoft.Dynamics.Ax.Tms.Bll.MileageRateEngine'e dayanan ve bir mesafe altyapısına başvuran bir değerlendirme altyapısı için gereken kurulum gösterilmektedir.
| Parametre             | Açıklama                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *RateBaseAssigner*    | Belirli bir şemaya yönelik değerlendirme taban ataması verilerini yorumlayan .NET türü. İki parametre değeri sözdizimi oluşur dikey ayrılmış kesimlerini çubuk ()|). İlk segment, atayıcı türünü tanımlayan derleme adını içerir. İkinci segment, atayıcı türünün tam adını tanımlar. Bu, türün ad alanını içerir. |
| *MileageEngineCode*   | Microsoft Dynamics 365 for Operations veritabanındaki mesafe altyapısı kaydını tanımlayan mesafe altyapısı kodu.                                                                                                                                                                                                                                                             |
| *ApportionmentEngine* | Microsoft Dynamics 365 for Operations veritabanındaki paylaştırma altyapısını tanımlayan genel altyapı kodu.                                                                                                                                                                                                                                                              |

 
<a name="how-is-metadata-used-in-transportation-management-engines"></a>Meta veriler, taşıma yönetimi altyapısında nasıl kullanılır?
----------------------------------------------------------

Dynamics 365 for Operations uygulamasında tanımlanan verilere dayanan taşıma yönetimi altyapıları farklı veri şemaları kullanabilir. Taşıma yönetimi sistemi, farklı taşıma yönetimi altyapılarının aynı genel fiziksel veritabanı tablolarını kullanmasına imkan verir. Altyapı verilerinin çalışma süresini doğru yorumlaması için, veritabanı tablolarına meta veri tanımlayabilirsiniz. Bu, yeni taşıma yönetimi altyapılarının inşa edilmesine yönelik maliyetleri azaltır çünkü Operations'da ek tablo ve form yapıları gerekmez.

## <a name="what-can-be-used-as-search-data-in-rate-calculations"></a>Değerlendirme hesaplamalarında arama verisi olarak ne kullanılabilir?
Microsoft Dynamics 365 for Operations'da oranları hesaplarken kullandığınız veri, meta veri yapılandırması tarafından kontrol edilir. Örneğin, posta kodlarına göre oranları aramak istiyorsanız, posta kodu arama türüne göre meta veri ayarlamanız gerekir.

## <a name="do-all-engine-configurations-require-metadata"></a>Tüm altyapı yapılandırmaları meta veri gerektirir mi?
Hayır, harici sistemlerden oran hesaplamak için gereken verileri almada kullanılan taşıma yönetimi altyapıları meta veri gerektirmez. Bu altyapılara yönelik oran verileri, harici taşıma taşıyıcı sistemlerinden, genellikle bir web hizmeti üzerinden alınabilir. Örneğin, doğrudan Bing haritalarından veri alan bir mesafe altyapısı kullanabilir, böylece bu altyapı için meta veriye ihtiyaç duymazsınız.
| **Not **                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Microsoft Dynamics 365 for Operations ile birlikte sağlanan taşımacı yönetimi altyapıları uygulamadan alınan verileri kullanır. Operations, harici sistemlere bağlanan altyapıları içermez. Ancak, altyapı tabanlı genişletilebilirlik modeli Microsoft Dynamics 365 for Operations Visual Studio Araçları kullanarak uzantılar oluşturmanızı sağlar. |

## <a name="how-do-i-configure-metadata-for-a-transportation-management-engine"></a>Bir taşıma yönetimi altyapısı için nasıl meta veri yapılandırabilirim?
Taşıma yönetimi altyapısına yönelik meta veriler, farklı altyapı türleri için farklı şekilde yapılandırılır.

| Taşıma yönetimi altyapısı               | Meta veri yapılandırması                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Değerlendirme altyapısı**                                | **Oran bazlı tür** gerektirir. Oran bazlı tür, oran bazlı veri ve oran bazlı atama verisi için meta veriler içerir. Oran bazlı meta verinin yapısı, değerlendirme altyapısının türü tarafından belirlenir. Oran bazlı atama meta verisinin yapısı, değerlendirme altyapısı ile ilişkili oran bazlı atayıcının türü tarafından belirlenir. Değerlendirme altyapısının oran bazlı türünü **Değerlendirme altyapısı** sayfasında ve **Ana oran** sayfasında ayarlayın. |
| **Bölge altyapısı**                                | Meta verilerin doğrudan ana bölgede ayarlanmasını gerektirir.                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Transit zamanı altyapısı** ve **Mesafe altyapısı** | Meta verileri doğrudan mesafe altyapısının yapılandırma kurulum formundan alır.                                                                                                                                                                                                                                                                                                                                                                                  |

  **Değerlendirme altyapısı için meta veri örneği** Taşıma yönetimi altyapısı, kaynak adresin, hedef ilin ve ülke/bölgenin ve sevkıyatın başlangıç ve bitiş noktasının tanımlanmasını gerektirir. Bu gereksinimleri kullanarak, meta veriler aşağıdaki tablodaki gibi görünecektir. Tablo ayrıca hangi veri girişi türü gerektiği hakkında bilgi de içermektedir.
-   Bu bilgileri tanımlamak **taşımacılık Yönetimi**&gt;**Kurulum** üzerinde **oranı temel tür** sayfa.

| Seri | Dosya Adı                          | Alan türü | Veri tipi | Arama türü    | Zorunlu |
|----------|-------------------------------|------------|-----------|----------------|-----------|
| 1        | Kaynak posta kodu            | Atama | Dize    | Posta Kodu    | Seçildi  |
| 2        | Hedef il             | Atama | Dize    | Eyalet          |           |
| 3        | Hedef başlangıç posta kodu | Atama | Dize    | Posta Kodu    | Seçildi  |
| 4        | Hedef bitiş posta kodu   | Atama | Dize    | Posta Kodu    | Seçildi  |
| 5        | Hedef ülke           | Atama | Dize    | Ülke/bölge |           |





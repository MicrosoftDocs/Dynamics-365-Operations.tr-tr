---
title: Taşıma yönetimi altyapıları
description: Nakliye yönetimi motorları, Nakliye yönetimindeki nakliye oranlarının oluşturulması ve işlenmesi için kullanılan mantığı tanımlar.
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSFreightBillType, TMSGenericEngine, TMSMileageEngine, TMSRateEngine, TMSTransitTimeEngine, TMSZoneEngine, TMSFreightBillTypeAssignment, TMSZoneMaster, TMSEngineParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 12234
ms.assetid: b878478c-0e04-4a1e-a037-6fdbb345a9a3
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e59fe56bc34e7412466daaeb04564aa3349f60e0370364b7ce5184a5785a278c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740587"
---
# <a name="transportation-management-engines"></a>Taşıma yönetimi altyapıları

[!include [banner](../includes/banner.md)]

Nakliye yönetimi motorları, Nakliye yönetimindeki nakliye oranlarının oluşturulması ve işlenmesi için kullanılan mantığı tanımlar. 

Bir taşıma yönetimi altyapısı, taşıyıcının ulaşım hızı gibi görevleri hesaplar. Altyapı sistemi, Supply Chain Management verilerini temel alan çalışma zamanında, hesaplama stratejileri değiştirmenize olanak tanır. Taşıma yönetimi altyapısı, belirli bir taşıyıcı sözleşmesiyle ilişkili bir eklentiye benzer.

## <a name="what-engines-are-available"></a>Hangi altyapılar var?
Aşağıdaki tabloda, kullanılabilecek taşıma yönetimi altyapıları gösterilmektedir.

| Taşıma yönetimi altyapısı | Tanım                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Değerlendirme altyapısı**                  | Oranları hesaplar.                                                                                                                                                                                                                                                                                                           |
| **Genel altyapı**               | Supply Chain Management'tan veri istemeyen diğer altyapılar için kullanılan basit yedek altyapılar (örneğin bir paylaştırma altyapısı). Paylaştırma altyapıları, belirli siparişlere ve satırlara taşımanın nihai maliyetlerini, hacim ve ağırlık gibi boyutlara dayalı olarak azaltmak için kullanılır. |
| **Mesafe altyapısı**               | Taşıma mesafesini hesaplar.                                                                                                                                                                                                                                                                                     |
| **Yoldaki süre altyapısı**          | Başlangıçtan son hedefe seyahat için gereken süreyi hesaplar.                                                                                                                                                                                                                                       |
| **Bölge altyapısı**                  | Geçerli adrese dayalı olarak bölgeyi hesaplar ve A adresinden B adresine gitmek için geçilmesi gereken bölge sayısını hesaplar.                                                                                                                                                                    |
| **Navlun fatura türü**            | Navlun faturasını ve navlun faturası satırlarını standartlaştırır ve otomatik navlun faturası eşleştirmesi için kullanılır.                                                                                                                                                                                                                |


## <a name="what-engines-must-be-configured-to-rate-a-shipment"></a>Bir sevkıyatı değerlendirmek için hangi altyapılar yapılandırılmalıdır?

Bir sevkıyatı belirli bir taşıyıcı kullanarak değerlendirmek için, birden fazla taşıma yönetimi altyapısı yapılandırmanız gerekir. **Değerlendirme altyapısı** gereklidir, ancak **Değerlendirme altyapısı**'nı desteklemek için diğer taşıma yönetimi altyapıları gerekebilir. Örneğin, **Değerlendirme altyapısı**, değerlendirmeyi kaynak ile hedef arasındaki mesafeye dayalı olarak hesaplamak için **Mesafe altyapısı**'ndan veri almak için kullanılabilir.

## <a name="whats-required-to-initialize-a-transportation-management-engine"></a>Bir taşıma yönetimi altyapısını başlatmak için ne gerekir?
Taşıma yönetimi altyapısı, belirli bir şekilde işlemesi için başlangıç verileri ayarlamanızı gerektirir. Kurulum aşağıdaki veri türlerini içerebilir:
-   Diğer taşıma yönetimi altyapılarına başvurur. Ayrıntılar için, bu bölümdeki yapılandırma örneğine bakın.
-   Taşıma yönetimi altyapısı tarafından kullanılan .NET türlerine başvurur.
-   Basit yapılandırma verileri.

Birçok durumda, taşıma yönetimi altyapısının kurulum formlarındaki **Parametreler** düğmesine tıklayarak başlangıç verilerini yapılandırabilirsiniz. **Bir mesafe altyapısına başvuran bir değerlendirme altyapısının yapılandırılmasına dair örnek** Aşağıdaki örnekte, .NET altyapısı türü Microsoft.Dynamics.Ax.Tms.Bll.MileageRateEngine'e dayanan ve bir mesafe altyapısına başvuran bir değerlendirme altyapısı için gereken kurulum gösterilmektedir.

|          Parametre           |                                                                                  Açıklama                                                                                  |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <em>RateBaseAssigner</em>   | Belirli bir şemaya yönelik değerlendirme taban ataması verilerini yorumlayan .NET türü. Parametre değerinin sözdizimi dikey bir çubukla (|) ayrılmış iki segmentten oluşur ( |
|  <em>MileageEngineCode</em>  |                       Veritabanında mesafe altyapısı kaydını tanımlayan mesafe altyapısı kodu.                        |
| <em>ApportionmentEngine</em> |                        Veritabanında paylaştırma altyapısını tanımlayan genel altyapı kodu.                        |

## <a name="how-is-metadata-used-in-transportation-management-engines"></a>Meta veriler, taşıma yönetimi altyapısında nasıl kullanılır?

Supply Chain Management'ta tanımlanmış verilere dayanan taşıma yönetimi altyapıları, farklı veri şemaları kullanabilir. Taşıma yönetimi sistemi, farklı taşıma yönetimi altyapılarının aynı genel fiziksel veritabanı tablolarını kullanmasına imkan verir. Altyapı verilerinin çalışma süresini doğru yorumlaması için, veritabanı tablolarına meta veri tanımlayabilirsiniz. Bu, yeni taşıma yönetimi altyapılarının inşa edilmesine yönelik maliyetleri azaltır çünkü Operations'da ek tablo ve form yapıları gerekmez.

## <a name="what-can-be-used-as-search-data-in-rate-calculations"></a>Değerlendirme hesaplamalarında arama verisi olarak ne kullanılabilir?
Oranları hesaplarken kullandığınız veri, meta veri yapılandırması tarafından denetlenir. Örneğin, posta kodlarına göre oranları aramak istiyorsanız, posta kodu arama türüne göre meta veri ayarlamanız gerekir.

## <a name="do-all-engine-configurations-require-metadata"></a>Tüm altyapı yapılandırmaları meta veri gerektirir mi?
Hayır, harici sistemlerden oran hesaplamak için gereken verileri almada kullanılan taşıma yönetimi altyapıları meta veri gerektirmez. Bu altyapılara yönelik oran verileri, harici taşıma taşıyıcı sistemlerinden, genellikle bir web hizmeti üzerinden alınabilir. Örneğin, doğrudan Bing haritalarından veri alan bir mesafe altyapısı kullanabilir, böylece bu altyapı için meta veriye ihtiyaç duymazsınız.

| **Not**                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Supply Chain Management'la birlikte sağlanan taşımacı yönetimi altyapıları, uygulamadan alınan verileri kullanır. Operations, harici sistemlere bağlanan altyapıları içermez. Ancak, altyapı tabanlı genişletilebilirlik modeli, Visual Studio Araçları kullanarak uzantılar yapmanıza olanak sağlar. |

## <a name="how-do-i-configure-metadata-for-a-transportation-management-engine"></a>Bir taşıma yönetimi altyapısı için nasıl meta veri yapılandırabilirim?
Taşıma yönetimi altyapısına yönelik meta veriler, farklı altyapı türleri için farklı şekilde yapılandırılır.

| Taşıma yönetimi altyapısı               | Meta veri yapılandırması                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Değerlendirme altyapısı**                                | **Oran bazlı tür** gerektirir. Oran bazlı tür, oran bazlı veri ve oran bazlı atama verisi için meta veriler içerir. Oran bazlı meta verinin yapısı, değerlendirme altyapısının türü tarafından belirlenir. Oran bazlı atama meta verisinin yapısı, değerlendirme altyapısı ile ilişkili oran bazlı atayıcının türü tarafından belirlenir. Değerlendirme altyapısının oran bazlı türünü **Değerlendirme altyapısı** sayfasında ve **Ana oran** sayfasında ayarlayın. |
| **Bölge altyapısı**                                | Meta verilerin doğrudan ana bölgede ayarlanmasını gerektirir.                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Transit zamanı altyapısı** ve **Mesafe altyapısı** | Meta verileri doğrudan mesafe altyapısının yapılandırma kurulum formundan alır.                                                                                                                                                                                                                                                                                                                                                                                  |

  **Değerlendirme altyapısı için meta veri örneği** Taşıma yönetimi altyapısı, kaynak adresin, hedef ilin ve ülke/bölgenin ve sevkıyatın başlangıç ve bitiş noktasının tanımlanmasını gerektirir. Bu gereksinimleri kullanarak, meta veriler aşağıdaki tablodaki gibi görünecektir. Tablo ayrıca hangi veri girişi türü gerektiği hakkında bilgi de içermektedir.
-   Bu bilgileri **Oran bazlı tür** sayfasında **Taşıma yönetimi** &gt; **Kurulum**'da tanımlayın.

| Seri | Dosya Adı                          | Alan türü | Veri tipi | Arama türü    | Zorunlu |
|----------|-------------------------------|------------|-----------|----------------|-----------|
| 1        | Kaynak posta kodu            | Atama | Dize    | Posta Kodu    | Seçildi  |
| 2        | Hedef il             | Atama | Dize    | Eyalet          |           |
| 3        | Hedef başlangıç posta kodu | Atama | Dize    | Posta Kodu    | Seçildi  |
| 4        | Hedef bitiş posta kodu   | Atama | Dize    | Posta Kodu    | Seçili  |
| 5        | Hedef ülke           | Assignment | Dize    | Ülke/bölge |           |

### <a name="whitepaper"></a>Teknik inceleme

Daha fazla bilgi için, aşağıdaki teknik incelemeyi indirin (AX2012'yi desteklemek için yazılmıştır ancak Dynamics 365 Supply Chain Management için de geçerlidir)

- [Taşıma yönetimi altyapıları](https://download.microsoft.com/download/e/0/9/e0957665-c12f-43c7-94c0-611cc49d7d61/TransportationManagementEnginesInAX.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
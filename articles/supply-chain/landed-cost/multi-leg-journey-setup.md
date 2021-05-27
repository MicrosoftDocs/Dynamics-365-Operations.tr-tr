---
title: Çok duraklı yolculuk kurulumu
description: Bu konuda, Varış yeri maliyeti modülü için çok duraklı yolculukların nasıl ayarlanacağı açıklanmaktadır.
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMLegTable, ITMJourneyTable, ITMActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 45e32c59c79389bcab15dd07d1bbd33d7ff34340
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021576"
---
# <a name="multi-leg-journey-setup"></a>Çok duraklı yolculuk kurulumu

[!include [banner](../../includes/banner.md)]

Bu konuda, **Varış yeri maliyeti** modülü için çok duraklı yolculukların nasıl ayarlanacağı açıklanmaktadır.

## <a name="legs"></a>Duraklar

Duraklar bir yolculuğun ayrı kısımlarını tanımlamak için kullanılır. Her durak, "varış" ve "çıkış" sevkiyat limanları ve bu durak için kullanılan taşıma modu seçilerek oluşturulur. Sağlama süreleri her durakla ilişkilendirilebilir. Sağlama süreleri bir sevkiyatı izlemeye yardımcı olabilir ve bir seyahatte malların tahmini teslimat tarihini hesaplamak için de kullanılabilir. Ayrıca, bir yolculuğun bir durağı tamamlandığında, seyahat, sevkiyat konteyneri ve ilişkili satın alma siparişi satırlarının durumu izleme denetimi kurulumu aracılığıyla güncellenebilir. Duraklar tek bir yolculuk şablonu tarafından kullanılabilir veya birden çok yolculuk şablonu tarafından yeniden kullanılabilir. Konteyner yükleme, gümrük ve yerel taşıma genellikle durak olarak ayarlanır ve bunlar için özel olmayan bir sevkiyat limanı kullanılır.

Duraklarla çalışmak için **Varış yeri maliyeti \> Çok duraklı yolculuk kurulumu \> Duraklar**'a gidin. Burada, duraklar için kayıtları görüntüleyebilir, açabilir, oluşturabilir ve silebilirsiniz. Aşağıdaki tabloda, her kayıtta kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Durak | Yolculuk durağı için benzersiz bir tanımlama adı/numarası girin. |
| Tanım | Yolculuk durağı için açıklama girin. Genellikle, bu açıklama "varış" ve "çıkış" limanlarını veya yolculuğun adımını tanımlar. |
| Çıkış limanı | Duraktaki malların çıkış noktasını girin. |
| Varış limanı | Duraktaki malların varış noktasını girin. |
| Teslimat yöntemi | Durak için taşıma yöntemini girin. |

## <a name="journey-templates"></a>Yolculuk şablonları

Bir yolculuk şablonu, malların bir yolculuk sırasında seyahat ettiği iki liman arasındaki çok duraklı yolculuğu tanımlar. Yolculuğun durakları, malların satıcının çıkış noktasından son ambar hedefine gitmesi için gereken süreyi belirlemek için birleştirilir. Duraklar belirli bir sırada yolculuk şablonuna konduğunda, sağlama süreleri her durağın tarihini ve seyahat için seyahat, konteyner ve satın alma satırlarının durumunu tanımlar. Yolculuk şablonunu oluşturan her durakla ilişkili sağlama sürelerini ayarlamak için [İzleme denetim merkezini](delivery-information-setup.md) kullanın. Yolculuk şablonu, bir seyahatin otomatik maliyetleri ayarlandığında da kullanılır. Bir yolculuk tanımlandığında, malların taşınmasıyla ilişkili maliyet otomatik maliyetler sayfasında tanımlanabilir.

Yolculuk şablonlarıyla çalışmak için **Varış yeri maliyeti \> Çok duraklı yolculuk kurulumu \> Yolculuk şablonları**'na gidin. Burada, yolculuk şablonlarını görüntüleyebilir, açabilir, oluşturabilir ve silebilirsiniz.

Her yolculuk şablonu için başlıkta aşağıdaki alanları ayarlayın.

| Alan | Tanım |
|---|---|
| Yolculuk şablonu | Yolculuk şablonu için benzersiz bir tanımlama adı/numarası girin. Yolculuk şablonu genellikle yolculuğun başlangıç noktasını ve varış noktasını açıklar. |
| Tanım | Yolculuk şablonu için açıklama girin. Açıklama genellikle "varış" ve "çıkış" limanlarını ve seyahat türünü gösterir. |

**Satırlar** bölümünde, yolculuğun her durağı için bir satır ekleyin ve satırları sıraya koyun. Satırların sırasını değiştirmek için araç çubuğundaki **Yukarı** ve **Aşağı** oklarını kullanın. Aşağıdaki tabloda, her satırda kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Durak | Yolculuğa eklemek için bir durak seçin. |
| Tanım | Durak açıklaması. |
| Çıkış limanı | Duraktaki malların çıkış noktası olan liman. Bu liman, bir seyahatin otomatik maliyetlerini belirlemek için kullanılan "varış" limanıdır. |
| Varış limanı | Duraktaki malların son varış noktası. |
| Teslimat şekli | Durak için kullanılan teslimat şekli. |
| Yolculuk çıkış limanı | Durak için belirtilen liman otomatik maliyetleri belirlemek için kullanılıyorsa "yolculuk çıkış" limanı olarak tanımlamak için bu onay kutusunu seçin. Bu liman yolculuk başlığında gösterilecektir. |
| Yolculuk varış limanı | Durak için belirtilen liman otomatik maliyetleri belirlemek için kullanılıyorsa "yolculuk varış" limanı olarak tanımlamak için bu onay kutusunu seçin. Bu liman yolculuk başlığında gösterilecektir. |
| Sevkiyat şirketi | Durak için kullanılan sevkiyat şirketini seçin. |

## <a name="activities"></a>Faaliyetler

**Etkinlikler** sayfasındaki ayarlar, bir durağın hedef bağlantı noktasında oluşabilecek etkinlik türlerini belirler. **Tüm sevkiyat konteynerleri** sayfasında çalışan kullanıcılar, her etkinliğin süresini tahmin ettiklerinde ve karşılaştırma amacıyla gerçek süreyi kaydettiklerinde bu değerler arasından seçim yapabilir.

Etkinliklerinizi ayarlamak için **Varış yeri maliyeti \> Çok duraklı yolculuk kurulumu \> Etkinlikler**'e gidin. Buradan, eylem bölmesindeki düğmeleri kullanarak etkinlikleri ekleyebilir, kaldırabilir ve düzenleyebilirsiniz.

Aşağıdaki tabloda, kılavuzdaki her etkinlikte kullanılabilecek alanlar açıklanmıştır.

| Alan | Tanım |
|---|---|
| Faaliyet | Etkinlik adı. |
| Tanım | Etkinlik açıklaması. |
| Sevkiyat şirketi | Etkinlikle ilişkili sevkiyat şirketinin satıcı hesabı. |

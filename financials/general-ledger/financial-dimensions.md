---
title: Mali boyutlar
description: "Bu makalede, farklı mali boyut türleri ve nasıl ayarlandıkları açıklanmaktadır."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25871
ms.assetid: af54621c-c8be-4b72-b6df-dcf886c40ce4
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 5ee2d132f0b23ceec2a79ee6b0ee33862d6a0518
ms.contentlocale: tr-tr
ms.lasthandoff: 04/25/2017


---

# <a name="financial-dimensions"></a>Mali boyutlar

[!include[banner](../includes/banner.md)]


Bu makalede, farklı mali boyut türleri ve nasıl ayarlandıkları açıklanmaktadır.

Hesap planları içim hesap segmentleri olarak kullanabileceğiniz mali boyutlar oluşturmak için Mali boyutlar sayfasını kullanın. İki tür mali boyut vardır: özel boyutlar ve varlığa dayalı boyutlar. Özel boyutlar tüzel kişilikler tarafından paylaşılır ve değerler kullanıcı tarafından girilir ve korunur. Varlığa dayalı boyutlar, değerleri sistemin herhangi bir bölümünde tanımlanan (Müşteriler veya Mağazalar gibi) boyutlardır. Bazı varlığa dayalı boyutlar tüzel kişilikler tarafından paylaşılır ve şirkete özel boyutlar olur. 

Mali boyutları oluşturduktan sonra, her mali boyuta ek özellikler atamak için Mali boyut değerleri sayfasını kullanın. 

Microsoft Dynamics 365 for Operations'da tüzel kişilikler oluşturmadan mali boyutları tüzel kişilikleri temsil etmek amacıyla kullanabilmenize karşın, mali boyutlar tüzel kişiliklerin operasyonel veya iş gereksinimlerini karşılamak üzere tasarlanmamıştır. Microsoft Dynamics 365 for Operations'daki birimlerarası muhasebe işlevi, yalnızca her hareket tarafından oluşturulan muhasebe girişlerini karşılamak üzere tasarlanmıştır. 

Mali boyutları tüzel kişilikler olarak ayarlamadan önce, bu ayarın kuruluşunuz için uygun olup olmadığını belirlemek üzere iş süreçlerini aşağıdaki alanlarda değerlendirin:

-   Stok
-   Mali boyutlar ile tüzel kişilikler arasındaki satışlar ve satınalmalar
-   Satış vergisi hesaplama ve bildirme
-   Operasyonel raporlama

Aşağıda sınırlamalara ilişkin bazı örnekler verilmektedir:

-   Satış vergisi işlevini yalnızca tüzel kişiliklerle kullanabilirsiniz; mali boyutlarla birlikte kullanamazsınız.
-   Bazı raporlar mali boyutları içermez. Bu nedenle, bu raporlar değiştirilmediği sürece her zaman finansal boyuta göre raporlama yapamazsınız.

**Özel boyutlar** 

Kullanıcı tanımlı bir mali boyut oluşturmak için, Kullan değerin kaynağı alanından, &lt;Özel boyut&gt;'u seçin. Boyut değerleri için girebileceğiniz bilgi miktarını ve türünü sınırlamak üzere bir hesap maskesi de belirtebilirsiniz. Harf veya tire gibi her boyut değeri için aynı kalan karakter girebilirsiniz. Bir boyut değeri her oluşturulduğunda değişen harfler ve sayılar için yer tutucular olan sayı işaretleri (\#) ve 've' işaretleri (&) de girebilirsiniz. Bir sayının yer tutucusu olarak sayı işareti (\#) ve bir harfin yer tutucusu olarak ve işareti (&) kullanın. 

**Örnek** 

Örnek: Boyutu CC harfleri ve üç sayıyla sınırlamak için biçim maskesi olarak CC-\#\#\# girin. Bu alan yalnızca Kullanılacak değerlerin kaynağı alanında &lt; Özel boyut &gt; öğesini seçtiğinizde kullanılabilir. 

**Varlık dayalı boyutlar** 

Varlığa dayalı boyut oluşturmak için, Kullanılacak değerlerin kaynağı alanından, mali boyuta temel alınacak bir sistem tanımlı varlık seçin. Mali boyut değerleri bu seçimden oluşturulur. Örneğin, projeler için boyut değerleri oluşturmak üzere Projeleri seçin. Her proje adı için bir boyut değeri oluşturulur. Boyur değerleri sayfası, varlığa ait değerleri ve değerler şirkete özelse, değerle ilgili şirketi gösterir. 

**Boyutları etkinleştirme** 

Mali boyut etkinleştirmesi tabloyu mali boyut adıyla güncelleştirir ve silinen boyutları kaldırır. Mali boyutu etkinleştirmeden önce boyut değerleri girebilirsiniz ancak mali boyut etkinleştirilene kadar hiçbir yerde kullanılamaz. Örneğin, mali boyut etkinleştirilene kadar bir hesap yapısına bir mali boyut ekleyemezsiniz. Etkinleştir'e tıkladığınızda, tüm boyutlar durum değişiklikleriyle güncelleştirilir. 

**Çeviriler** 

Metin çevirisi sayfası, seçili mali boyut için farklı dillerde görüntülenecek metni girmenize olanak tanır. Ana hesap çeviri sayfası, ana hesap için farklı dillerde görüntülenecek bir metin girebileceğiniz alandır. 

**Tüzel varlık geçersiz kılmaları** 

Tüm yasal birimler için tüm boyutlar geçerli değildir, bazı ana hesaplar sadece belirli bir zaman aralığı için geçerli olabilir. Bu senaryoda, Tüzel kişilik geçersiz kılma bölümü, boyutun hangi şirketler için askıya alınacağını, sahibinin kim olduğunu ve boyutun etkin olacağı zaman dilimini tanımlamak için kullanılabilir.







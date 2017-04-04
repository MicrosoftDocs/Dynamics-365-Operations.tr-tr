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
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: f849b98cac88d182875aca88aaf04cd3575ed99f
ms.lasthandoff: 03/31/2017


---

# <a name="financial-dimensions"></a>Mali boyutlar

Bu makalede, farklı mali boyut türleri ve nasıl ayarlandıkları açıklanmaktadır.

Hesap planları içim hesap segmentleri olarak kullanabileceğiniz mali boyutlar oluşturmak için Mali boyutlar sayfasını kullanın. İki tür mali boyut vardır: özel boyutlar ve varlığa dayalı boyutlar. Özel boyutlar tüzel kişilikler tarafından paylaşılır ve değerler kullanıcı tarafından girilir ve korunur. Varlığa dayalı boyutlar, değerleri sistemin herhangi bir bölümünde tanımlanan (Müşteriler veya Mağazalar gibi) boyutlardır. Bazı varlığa dayalı boyutlar tüzel kişilikler tarafından paylaşılır ve şirkete özel boyutlar olur. 

Mali boyutları oluşturduktan sonra, her mali boyuta ek özellikler atamak için Mali boyut değerleri sayfasını kullanın. 

İşlemler için Microsoft Dynamics 365 tüzel kişilikler oluşturmak zorunda kalmadan yasal tüzel kişileri temsil etmek için mali boyutları kullanabilseniz de, mali boyutları operasyonel gidermek üzere tasarlanmamış veya iş tüzel kişilikler gerek. Microsoft Dynamics 365 işlemleri için interunit hesap işlevleri her hareketin oluşturduğu muhasebe girişleri karşılayacak şekilde tasarlanmıştır. 

Mali boyutları tüzel kişilikler olarak ayarlamadan önce, bu ayarın kuruluşunuz için uygun olup olmadığını belirlemek üzere iş süreçlerini aşağıdaki alanlarda değerlendirin:

-   Stok
-   Mali boyutlar ile tüzel kişilikler arasındaki satışlar ve satınalmalar
-   Satış vergisi hesaplama ve bildirme
-   Operasyonel raporlama

Aşağıda sınırlamalara ilişkin bazı örnekler verilmektedir:

-   Satış vergisi işlevini yalnızca tüzel kişiliklerle kullanabilirsiniz; mali boyutlarla birlikte kullanamazsınız.
-   Bazı raporlar mali boyutları içermez. Bu nedenle, bu raporlar değiştirilmediği sürece her zaman finansal boyuta göre raporlama yapamazsınız.

**Custom dimensions** 

Kullanım değerleri alanından bir kullanıcı tarafından tanımlanan finansal boyut oluşturmak için seçin &lt;Özel boyut&gt;. Boyut değerleri için girebileceğiniz bilgi miktarını ve türünü sınırlamak üzere bir hesap maskesi de belirtebilirsiniz. Harf veya tire gibi her boyut değeri için aynı kalan karakter girebilirsiniz. Numara işareti de girebilirsiniz (\#) ve ve işaretleri (&) harfler ve boyut değeri oluşturan her zaman değişen sayılar için yer tutucu olarak. Sayı işareti kullanın (\#) bir harf için bir yer tutucu olarak bir sayı ve bir ampersan için yer tutucu olarak (&). 

**Example** 

Üç rakam ve harf CC boyut değerine sınırlamak için CC - girmeniz\#\#\# format maskesi olarak. Bu alan yalnızca seçtiğinizde kullanılabilir &lt;Özel boyut &gt;alanından kullanım değerleri. 

**Yedeklenen varlık boyutları** 

Yedeklenen varlık mali boyut alanından kullanım değerleri oluşturmak için temel mali boyut için sistem tarafından tanımlanan bir varlık seçin. Mali boyut değerleri bu seçimden oluşturulur. Örneğin, projeler için boyut değerleri oluşturmak üzere Projeleri seçin. Her proje adı için bir boyut değeri oluşturulur. Boyur değerleri sayfası, varlığa ait değerleri ve değerler şirkete özelse, değerle ilgili şirketi gösterir. 

**Boyutlarını etkinleştirme** 

Mali boyut etkinleştirmesi tabloyu mali boyut adıyla güncelleştirir ve silinen boyutları kaldırır. Mali boyutu etkinleştirmeden önce boyut değerleri girebilirsiniz ancak mali boyut etkinleştirilene kadar hiçbir yerde kullanılamaz. Örneğin, mali boyut etkinleştirilene kadar bir hesap yapısına bir mali boyut ekleyemezsiniz. Etkinleştir'e tıkladığınızda, tüm boyutlar durum değişiklikleriyle güncelleştirilir. 

**Translations** 

Metin çeviri sayfası seçili mali boyut için farklı dillerde görüntülenecek metin girmenizi sağlar. Ana hesap çeviri sayfası, ana hesap için farklı dillerde görüntülenecek bir metin girebileceğiniz alandır. 

**Legal entity overrides** 

Tüm boyutları tüm tüzel kişilikler için geçerlidir ve yalnızca belirli bir süre için ilgili olabilir. Bu senaryoda, Tüzel kişilik geçersiz kılma bölümü, boyutun hangi şirketler için askıya alınacağını, sahibinin kim olduğunu ve boyutun etkin olacağı zaman dilimini tanımlamak için kullanılabilir.





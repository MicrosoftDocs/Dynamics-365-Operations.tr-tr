---
title: Değer modelleri ayarlama
description: Bu yordam, yeni bir sabit kıymet defterini nasıl oluşturacağınızı ve bir sabit kıymet grubuyla nasıl ilişkilendireceğinizi gösterir.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a528bd12552d5ce100027c9a789f6e1bdc597b66
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839773"
---
# <a name="set-up-value-models"></a>Değer modelleri ayarlama

[!include [task guide banner](../../includes/task-guide-banner.md)]

Bu yordam, yeni bir sabit kıymet defterini nasıl oluşturacağınızı ve bir sabit kıymet grubuyla nasıl ilişkilendireceğinizi gösterir. Muhasebeci rolünü ve USMF adlı tüzel kişilik için tanıtım verilerini kullanır.


## <a name="create-a-book"></a>Defter oluşturma
1. Sabit kıymetler > Kurulum > Defterler'e gidin.
2. Yeni'ye tıklayın.
3. Defter alanına bir değer yazın.
4. Açıklama alanına bir değer girin.
    * Amortismanı hesapla seçilirse, ilişkili kıymet defteri amortisman tekliflerine dahil edilir. Seçilmezse, kıymet defterine otomatik olarak amortisman uygulanmaz.  
5. Amortisman hesapla alanında Evet'i seçin.
6. Amortisman profili alanına bir değer girin veya seçin.
    * Alternatif bir amortisman profili de aynı zamanda amortisman geçiş yöntemi olarak bilinir. Alternatif profil, varsayılan amortisman profilininkine eşit veya ondan büyük bir amortisman tutarı hesaplarsa, amortisman teklifi bu profile geçer.  
    * Olağandışı durumlarda bir kıymetin ek amortismanı için Olağandışı amortisman profili kullanılır. Örneğin bunu doğal felaketlerden kaynaklanan amortismanı kaydetmek için kullanabilirsiniz.  
    * Temel düzeltmeler bulunan amortisman düzeltmeleri oluştur seçilirse, kıymetin değeri güncelleştirildiği zaman otomatik olarak amortisman düzeltmeleri oluşturulur. Seçilmezse, güncelleştirilmiş kıymet değeri yalnızca ilerideki amortisman hesaplamalarını etkiler.  
7. Temel düzeltmeler bulunan Amortisman düzeltmeleri oluştur alanında Evet'i seçin.
    * Varsayılan olarak, sabit kıymet defteri hareketlerini genel muhasebeye nakleder. Defter için genel muhasebeye nakil işlemini, Genel muhasebeye naklet alanını Hayır olarak ayarlayarak devre dışı bırakabilirsiniz. Genel muhasebeye nakledilmeyen defterler genellikle vergi raporlama amacıyla kullanılır. Bu, genel muhasebeye taahhütte bulunulmadığından kıymet defterine ait geçmiş hareketleri silmek için size ek bir esneklik sağlar.  
    * Defter genel muhasebeye nakledilirse deftere nakil katmanı, Geçerli katmanın varsayılan değeri olur ve genel muhasebeye nakledilmezse Hiçbiri olur. Bu defter için hareketlerin başka bir katmana nakledilmesi gerekiyorsa Deftere nakil katmanını güncelleştirin.  
8. Takvim alanına bir değer girin veya buradan bir değer seçin.
    * Türetilmiş defterler hareketleri aynı anda farklı defterlere nakleder. Hareketleri birincil defter ile oluşturursunuz ve deftere nakletme sırasında hareketin tam bir kopyası türev defterine nakledilir. Türev defteri hareketleriyle yeniden hesaplama olmaz, bu nedenle amortisman hareketlerinde kullanılmamalıdır.  

## <a name="associate-the-book-with-a-fixed-asset-group"></a>Defteri bir sabit kıymet grubuyla ilişkilendirin
1. Sabit kıymet grupları'na tıklayın.
2. Sabit kıymet grubu alanında bir değer girin veya seçin.
3. Servis ömrü alanına bir sayı girin.
    * Amortisman dönemlerinin, Servis ömrü ayarlandıktan sonra hesaplandığına dikkat edin.  
    * Amortisman yöntemini, vergi amaçları için gerektiği şekilde ayarlama olanağınız vardır.  


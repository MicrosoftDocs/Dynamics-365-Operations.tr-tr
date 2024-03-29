---
title: Gelişmiş banka mutabakatı kurulumu işlemi
description: Gelişmiş banka mutabakatı, elektronik banka ekstrelerini içe aktarmanıza ve bunların Microsoft Dynamics 365 Finance'teki banka hareketleriyle otomatik olarak mutabakat sağlamasına izin verir. Bu makalede mutabakat için işlem ayarları açıklanır.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: kfend
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9a1757f7901a12a5b0fc3de730953c5b79cbefb
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715456"
---
# <a name="advanced-bank-reconciliation-setup-process"></a>Gelişmiş banka mutabakatı kurulumu işlemi

[!include [banner](../includes/banner.md)]

Gelişmiş banka mutabakatı, elektronik banka ekstrelerini içe aktarmanıza ve bunların Microsoft Dynamics 365 Finance'teki banka hareketleriyle otomatik olarak mutabakat sağlamasına izin verir. Bu makalede mutabakat için işlem ayarları açıklanır.  

Gelişmiş banka mutabakatı işlevini kullanmadan önce ayarlanması gereken bir dizi parça vardır. Banka ekstresi içe aktarmayı ayarlama hakkında daha fazla bilgi için bkz. [Gelişmiş banka mutabakatı içe aktarma sürecini ayarlama](set-up-advanced-bank-reconciliation-import-process.md).  Banka mutabakatı işleminin kurulması için gereksinimler aşağıda açıklanmıştır.

## <a name="transaction-codes"></a>Hareket kodları
Hareket kodları, banka mutabakatı eşleştirme kurallarının parçası olarak kullanılabilir. Hareket kodları, Finance ve banka ekstreniz arasında yalnızca aynı türdeki hareketleri eşleştirmeye yardımcı olacaktır. Bu tür bir eşleştirme yapmak için öncelikle Finance içinden banka hareketleri için kullanılan hareket tiplerini tanımlamak, daha sonra bankanız tarafından kullanılan bu ekstre hareket kodlarını eşleştirmek gerekir. Banka hareketleri için hareket türleri, **Banka hareket türü** sayfasında tanımlanır. Burası ayrıca, söz konusu hareket türüyle defter nakillerini ilişkilendirmede kullanılacak ana hesabı tanımladığınız yerdir. 

Banka hareket kodlarınız tanımlandıktan sonra, bunları elektronik banka ekstrelerinde kullandığınız hareket kodlarına eşlersiniz. Bu eşleme işlemi **Hareket kodu eşleme** sayfası kullanılarak yapılır. Hareket kodu eşleme, her banka hesabı için tümüyle ayrıdır.

## <a name="matching-rules-and-matching-rule-sets"></a>Eşleştirme kuralları ve eşleştirme kural kümeleri
Eşleme kuralları, Finance banka hareketleri ve banka ekstresi hareketleri arasında otomatik mutabakat ölçütleri tanımlamanıza izin verir. Eşleşen kuralların ayarlanması **Mutabakat eşleme kuralları** sayfasında yapılır. Daha fazla bilgi için bkz. [Banka mutabakatı eşleme kuralları ayarlama](set-up-bank-reconciliation-matching-rules.md). 

Eşleştirme kuralı kümeleri, banka mutabakat işlemi sırasında çalıştırılacak bir eşleşme kuralı grubunu tanımlamak için kullanılır.  Eşleşen kura kümeleri **Mutabakat eşleme kuralı kümeleri** sayfasında yapılandırılır.

## <a name="cash-and-bank-management-parameters"></a>Nakit ve banka yönetimi parametreleri
**Nakit ve banka yönetim parametreleri** sayfası üzerinde, gelişmiş banka mutabakatı işlemine özel bir dizi parametre bulunmaktadır.  **Borç/alacak üzerinde ekstre satırı miktarını göster**, **Banka ekstresi** sayfası üzerindeki tutarların görünümünü değiştirir. Bu seçenek seçili ise, banka ekstresi hareket tutarları ayrı borç ve alacak sütunlarında görüntülenir. Seçilmemişse, banka ekstresi hareket tutarları, bir tek tutar sütununda uygun işaretle gösterilir. 

Parametre sayfası geçersiz kılma üzerindeki doğrulama seçenekleri, eşleşme kuralları üzerindeki seçimleri geçersiz kılar. Örneğin, belgeleri, parametreler sayfasında belirtilen tarih farkının ötesinde otomatik veya elle eşleştiremezsiniz. Ayrıca, **Hareket türü eşleme doğrulama** seçeneği işaretlenmişse, hareket türleri Finance banka hareketleri ve banka ekstresi hareketleri arasında, hareketlerin elle veya otomatik olarak eşleştirilmesi için eşleştirilmeleri gerekir. 

**Nakit ve banka yönetim parametreleri** üzerinde gerekli numara serilerini de yapılandırmanız gerekir.  **Numara serileri** sekmesinde İndirme **Kimlik Bilgisi, Ekstre Kimliği, Mutabakat Kimliği, Banka Kimliği** referanslarının numara seri kodlarını ayarlayın.

## <a name="bank-account-reconciliation-options"></a>Banka hesabı mutabakatı seçenekleri
İlk önce banka hesabı için Gelişmiş banka mutabakatını etkinleştirmeniz gerekir. Gelişmiş banka mutabakatı özelliği etkinleştirildikten sonra **Banka hesabı** sayfasında bir dizi ek seçenek kullanılabilecektir. 

**Elektronik ödeme onayı olarak banka ekstrelerini kullan** işlevi, banka mutabakatı işlevini, elektronik ödeme durumlarıyla birleştirir. Bu etkinleştirildiğinde, bir banka belgesi elektronik ödeme durumu **Gönderildi** olarak ayarlanmış için otomatik oluşturulur. Ek olarak, bir elektronik ödemenin durumu **Gönderildi**'den, **Alındı**'ya güncelleştirilecektir, ödeme eşleştikten, mutabakatı sağlandıktan ve deftere nakledildikten sonra. 

**Ekstrelerdeki banka hesabı adı** alanı, elektronik banka ekstrelerinizde kullanılan banka hesabınızın adıdır. Bu ad, bir banka hesabı için birden fazla banka hesabına ilişkin bilgi içeren bir ekstreden hangi hareketlerin alınacağını belirlerken kullanılır. 

**İçe aktarmadan sonra mutabakat sağla** seçeneği, banka ekstresini otomatik doğrulayacaktır, yeni bir banka mutabakatı ve çalışma sayfası oluşturacak ve Varsayılan eşleşme kural kümesini çalıştıracaktır. Bu işlev, el ile eşleştirilmesi gereken hareketlere kadar olan süreci otomatik hale getirir. Banka hesabındaki ayar içe alınırken varsayılana döner.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

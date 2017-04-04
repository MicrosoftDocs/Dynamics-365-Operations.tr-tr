---
title: "Gelişmiş banka mutabakatına genel bakış"
description: "Gelişmiş banka mutabakatı elektronik banka ekstrelerini içe aktarma ve otomatik olarak Microsoft Dynamics 365 işlemleri için banka hareketleri arasında mutabakat olanak sağlar.  Bu makalede mutabakat için işlem ayarları açıklanır."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: c2fc9e858f61d7d0122393bbf306ba64ac3659b8
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>Gelişmiş banka mutabakatına genel bakış

Gelişmiş banka mutabakatı elektronik banka ekstrelerini içe aktarma ve otomatik olarak Microsoft Dynamics 365 işlemleri için banka hareketleri arasında mutabakat olanak sağlar.  Bu makalede mutabakat için işlem ayarları açıklanır.  

Gelişmiş banka mutabakatı işlevini kullanmadan önce ayarlanmalıdır parçaları vardır. Banka ekstresi alma ayarlama hakkında daha fazla bilgi için bkz: [banka ekstresi alma işlemi kurmak](set-up-advanced-bank-reconciliation-import-process.md).  Mutabakat işlem kurulması için gereksinimleri aşağıda açıklanmıştır.

## <a name="transaction-codes"></a>Hareket kodları
Hareket kodlarını banka mutabakatı kurallarla eşleşen bir parçası olarak kullanılabilir.  Hareket kodlarını yalnızca aynı türde Dynamics 365 işlemleri için Banka ekstrenizde arasındaki işlemleri eşleştirmek için yardımcı olur.  Bu tür eşleştirme yapmak için öncelikle Dynamics 365 işlemleri için banka hareketleri için kullanılan hareket tiplerini tanımlamak, sonra gerekir, banka tarafından kullanılan deyim hareket kodları bu türleri eşleştirin.  Üzerinde tanımlanan işlemleri banka hareketlerinin hareket tipi için Dynamics 365 **banka hareket türü** sayfa.  Bu hareket türüyle ilgili defter nakilleri için kullanılacak ana hesap tanımladığınız budur. 

Banka işlemleri işlem kodları için Dynamics 365 tanımlanmış bir kez, sonra olanlar, elektronik banka deyimlerinde kullanılan işlem kodları için eşleyin.  Bu eşleme işlemi yapılır kullanarak **hareket kodu eşleme** sayfa.  Her banka hesabı için ayrı ayrı hareket kodu eşleme tamamlandı.

## <a name="matching-rules-and-matching-rule-sets"></a>Eşleştirme kuralları ve eşleştirme kural kümeleri
Eşleştirme kuralları otomatik işlemleri banka hareketleri için Dynamics 365 ve banka ekstresi hareketlerini mutabakatı için ölçüt tanımlamak izin verir.  Eşleştirme kuralları ayarlamak yapılır **eşleştirme kurallarını mutabakat** sayfa.  Daha fazla bilgi için bkz: [banka mutabakatı eşleştirme kurallarını ayarlamak](set-up-bank-reconciliation-matching-rules.md). 

Eşleşen kural kümeleri, bir grup sırayla banka mutabakat işlemi sırasında çalıştırılan eşleşen kurallar tanımlamak için kullanılır.  Eşleşen kural kümeleri üzerinde yapılandırılmış olan **eşleşen kural kümeleri mutabakat** sayfa.

## <a name="cash-and-bank-management-parameters"></a>Nakit ve banka yönetimi parametreleri
Parametre sayısı Gelişmiş banka mutabakat işlemi için özel **nakit ve Banka yönetimi parametrelerini** sayfa.  **Göster Ekstre Satır tutarı borç/alacak** üzerinde tutarlar görünümünü değiştirir **banka ekstresi** sayfa.  Bu seçenek seçili ise, banka ekstresi Hareket tutarlarını ayrı borç ve alacak sütunlarında görüntülenir.  Seçilmemişse, banka ekstresi Hareket tutarlarını bir tek Tutar sütununda uygun işaretiyle gösterilir. 

Eşleştirme kurallarını ayarlamak seçimleri ayarlanan parametreler sayfasında doğrulama seçenekleri geçersiz.  Örneğin, el ile veya otomatik olarak eşleşen belgeler parametreler sayfasında ayarlama tarihi fark ötesinde.  Ayrıca, varsa seçeneğini **hareket türü eşlemesi doğrulamak** olan seçilirse, hareket türlerini el ile veya otomatik olarak eşleştirilecek işlemleri banka hareketi için Dynamics 365 ve banka ekstresi hareketini hareketleri için sırayla arasında eşlenmesi gerekir. 

Üzerinde gerekli numara serilerini yapılandırmalısınız **nakit ve Banka yönetimi parametrelerini** sayfa.  Üzerinde **Number sequences** sekmesinde, karşıdan yükleme için numara serisi kodları kümesi **kimliği, deyim kimliği, mutabakat kimliği ve banka mutabakatı** başvurular.

## <a name="bank-account-reconciliation-options"></a>Banka hesabı mutabakatı seçenekleri
Gelişmiş banka mutabakatı banka hesabı için önce etkinleştirmeniz gerekir.  Ek seçenekler kullanılabilir **banka hesabı** Gelişmiş banka mutabakatı işlevi etkinleştirildiğinde sayfa. 

**Elektronik Ödeme onayı olarak kullanım Banka Ekstrelerini** işlevini elektronik Ödeme durumlarla banka mutabakatı işlevselliğini birleştirir.  Bu etkin olduğunda, elektronik Ödeme durumunu ayarlamak için Banka belge otomatik olarak oluşturulacak **gönderilen**.  Ayrıca, bir elektronik Ödeme durumu ile güncelleştirilir **gönderilen** için **alınan** ödeme eşleşti sonra mutabık ve deftere. 

**İfadeleri banka hesap adı**, elektronik Banka Ekstrelerini banka hesabı için kullanılan ad alanıdır.  Bu ad için birden fazla banka hesaplarına ilişkin bilgiler içerebilecek bir deyimi bir banka hesabından almak için hangi işlemleri belirlerken kullanılır. 

Seçeneği **alma sonra karşılaştırma** otomatik olarak banka ekstresi doğrulamak, yeni banka mutabakatı ve çalışma sayfası oluşturmak ve eşleşen kural kümesi varsayılan olarak çalışır.  Bu işlevsellik, hareketleri el ile eşlenmesi gereken noktaya kadar işlemini otomatikleştirir.  Banka hesabındaki ayar alırken varsayılan.



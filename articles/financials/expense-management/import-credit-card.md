---
title: "Kredi kartı hareketlerini içe aktarma ve yönetme"
description: "Bu konu, giderle ilişkili kredi kartı hareketlerinin nasıl içe aktarılacağını ve korunacağını açıklar. Bu hareketler, otomatik olarak yinelenen bir zamanlamada içe aktarılacak şekilde ayarlanabilir veya ihtiyaç duyuldukça el ile içe aktarılabilir."
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e640c9e44add5599be4a2e381b4ffd81f212889c
ms.contentlocale: tr-tr
ms.lasthandoff: 11/03/2017

---

# <a name="import-and-maintain-credit-card-transactions"></a>Kredi kartı hareketlerini içe aktarma ve yönetme

[!include[banner](../includes/banner.md)]

Giderle ilişkili kredi kartı hareketleri, yinelenen bir zamanlamada otomatik içe aktarılacak şekilde ayarlanabilir. Alternatif olarak, hareketler ihtiyaç duyuldukça el ile içe aktarılabilir. Kredi kartı hareketleri Kredi kartı hareketleri veri varlığı üzerinden içe aktarılır.

Veri varlıkları hakkında daha fazla bilgi için bkz. [Veri varlıkları](../../dev-itpro/data-entities/data-entities.md).

## <a name="import-credit-card-transactions"></a>Kredi kartı hareketlerini içe aktar

1. **Kredi kartı hareketleri** sayfasında, **Hareketleri içe aktar**'ı seçin. Veri yönetimini ilk kez açıyorsanız, devam etmeden önce sistemin veri varlıkları listesini güncelleştirmesi gerekir.
2. **Ad** alanında, içe aktarma işinin benzersiz bir açıklamasını girin.
3. **Kaynak veri biçimi** alanında, içe aktarılacak kredi kartı hareketlerini içeren dosyanın biçimini seçin.
4. **Karşıya yükle**'yi seçin ve içe aktarılacak dosyayı bulun ve seçin.
5. Dosya karşıya yüklendikten sonra, kutucuktaki **Görünüm eşleme** bağlantısına tıklayarak Kredi kartı hareketleri veri varlığı ve kredi kartı hareket dosyasının eşleşmesini doğrulayın. Eşleme hataları varsa veya eşlemeyi değiştirmeniz gerekiyorsa, eşleme değişikliklerini **Eşleme görselleştirme** sekmesi veya **Eşleme ayrıntıları** sekmesi üzerinden yapın.
6. Kredi kartı hareketlerini otomatikleştirmek için **Yinelenen bir veri işi oluştur** seçin. Daha sonra, kredi kartı hareketlerinin ne sıklıkta içe aktarılacağını belirten yinelemeyi ayarlayabilirsiniz. Tamamladıktan sonra **Tamam**'ı seçin.
7. Seçilen dosyayı şimdi içe aktarmak için **İçe aktar**'ı seçin.
8. İçe aktarma sırasında hatalar oluşursa, başarılı bir içe aktarmayı garanti etmeye yardımcı olmak için yürütme günlüğünü veya hazırlama verisini görüntüleyebilirsiniz.

> [!NOTE]
> Birden fazla dosya biçimi içe aktarmanız gerekiyorsa, her bir biçim türü için ayrı içe aktarma işleri oluşturmanız gerekir.

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>İşten çıkarılan personeller için kredi kartı hareketlerini yeniden atayın

Bir personel kaydı sonlandırıldıktan sonra, personelin Active Directory Etki Alanı Hizmetleri (AD DS) hesabı devre dışı bırakılır. Ancak, halen gider haline getirilecek ve ödenecek etkin kredi kartı hareketleri olabilir. **Kredi kartı hareketleri** sayfasından, ilişkili personelin işten çıkarıldığı her türlü kredi kartı hareketi için personeli yeniden atayabilirsiniz.

Bir veya daha fazla kredi kartı hareketi seçin ve sonra **Hareketleri yeniden ata**'yı seçin. Daha sonra kredi kartı hareketlerinin atanacağı başka bir çalışan seçebilirsiniz. Kredi kartı hareketleri yeniden atadıktan sonra, bunlar bir gider raporu için seçilebilir ve gider raporu geri ödemeleri için uygulanan sıradan işlemlerle ödenebilir.


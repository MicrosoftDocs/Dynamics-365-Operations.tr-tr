---
title: " Bağlılık şemalarını tanımlama"
description: Bu yordamı bir bağlılık şemasının nasıl tanımlanacağını açıklar.
author: jashanno
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e76bb7ea8319ad1f366692090435e47e9bf0d7b2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796814"
---
# <a name="define-loyalty-schemes"></a> Bağlılık şemalarını tanımlama

[!include [banner](../includes/banner.md)]

Bu yordamı bir bağlılık şemasının nasıl tanımlanacağını açıklar. Bağlılık şemaları, bağlılık programına ilişkin ödül kazanma ve kullanma kurallarıdır. Bu yordam, USRT demo veri şirketini kullanır.

1. Retail and Commerce > Müşteriler > Bağlılık > Bağlılık şemaları menüsüne gidin.
2. Yeni'yi tıklatın.
3. Şema kodu alanına bir değer girin.
4. Açıklama alanına bir değer girin.
5. Ad alanında, açılır menü düğmesine tıklayarak aramayı açın.
    * Bir bağlılık programı için birden fazla bağlılık şemanız olabilir. Bağlılık şemaları tüm kanallara ya da kanalların alt kümesine yönelik olabilir.  
6. Listede, istenen kaydı bulun ve seçin.
7. Listede, seçili satırdaki bağlantıya tıklayın.
8. Kaydet'i tıklatın.
9. Satır ekle'ye tıklayın.
10. Etkinlik türü alanında bir seçenek belirleyin.
    * Müşterilerin harcamalarına göre ödül kazanmalarını istiyorsanız Tutara göre ürün satın al seçeneğini seçin. Müşterilerin satın aldıkları ürün adedine göre ödül kazanmasını istiyorsanız, miktara göre ürün satın al seçeneğini seçin.  Müşterilerin ne veya ne kadar satınaldıklarından bağımsız olarak, her satış hareketi için ödül kazanmalarını istiyorsanız Satış hareketleri sayısı seçeneğini seçin.  
    * Bir kategori seçin. Kategori bu kazanç kuralının uygulanacağı ürünleri sınırlar.  
    * Kazanç kuralının tüm ürünler için geçerli olmasını istiyorsanız bu alanı boş bırakın.  
11. Etkinlik tutarı/miktarı alanına bir sayı girin.
    *  Satış hareketi sayısı etkinlik türünde, her zaman '1.0' değerini kullanmalısınız. Tutara göre satın al veya Miktara göre satın al etkinlik türlerinde, girilen değerin altındaki hiçbir hareket kazanç kuralını etkinleştirmeyecektir. Örneğin, etkinlik türü Tutara göre satın al olduğunda '10.00' değerini girerseniz, '9,00' değerindeki bir satış hareketi için ödül kazanılmaz.  
12. Etkinlik para birimi alanına bir değer yazın.
13. Ödül puanı kodu alanında, aramayı açmak için açılır menü düğmesine tıklayın.
14. Listede, seçili satırdaki bağlantıya tıklayın.
15. Ödül puanları alanına bir sayı girin.
    * Tutar türü ödül puanları, kazanılan tutarları ondalık değerlerle kaydeder. Örneğin, kazanç kuralı her 1 Kanada dolarlı harcama için 1 ödül puanı kazanılacağını belirtiyorsa ve müşteri 1,25 Kanada doları harcarsa, bu durumda müşteri 1,25 ödül puanı kazanacaktır. Miktar türü ödül puanları kazanılan tutarları tam sayı olarak kaydeder. Kazanç kuralı her 1 Kanada dolarlı harcama için 1 ödül puanı kazanılacağını belirten örneği kullanıldığında ve müşteri 1,25 Kanada doları harcadığında, bu durumda müşteri 1,0 ödül puanı kazanacaktır.  
16. Kaydet'e tıklayın.
17. Satır ekle'ye tıklayın.
    * Kullanım kuralları, bağlılık ödül yöntemi kullanıldığı zaman kullanılır.  
18. Ödül puanı kodu alanında, aramayı açmak için açılır menü düğmesine tıklayın.
    * Yalnızca kullanılabilir ödül puanları gösterilir.  
19. Listede, seçili satırdaki bağlantıya tıklayın.
20. Ödül puanları alanına bir sayı girin.
21. Kullanım türü alanında bir seçenek belirleyin.
    * Tutara göre ödemenin seçilmesi durumunda, Tutar veya miktar alanı para birimi değeri olarak işlem görür. Bu durumda, ödemenin para birimi başına kullanılan ödül puanlarının tutarı sabit bir orandır. Miktara göre ödeme seçeneğinin seçilmesi, Tutar veya miktar alanının bir miktar değeri olarak işlem görmesine yol açar. Bu durumda, madde miktarı başına kullanılan ödül puanlarının tutarı sabit bir orandır; ancak, para birimi cinsinden tutar, aynı miktar için bağlılık ödül puanlarıyla ödenen madde fiyatının farklılık göstermesi durumunda değişebilir. Bağlılık puanları iskontosu kullanım türü yalnızca 'Rusya' Ülkeye/Bölgeye özgü özellikleri yapılandırma anahtarı etkinleştirildiğinde ve POS işlevi profillerinde 'RU' için bir ISO kodu bulunduğunda geçerlidir.  
    * Bir kategori seçin. Kategori bu kullanım kuralının uygulanacağı ürünleri sınırlar.  
    * Kullanım kuralının tüm ürünler için geçerli olmasını istiyorsanız bu alanı boş bırakın.  
22. Tutar veya miktar alanına bir sayı girin.
23. Para birimi alanına bir değer yazın.
24. Kaydet'e tıklayın.
25. Satır ekle'ye tıklayın.
    * Kullanılabilir kuruluş düğümleri listesinden bir veya daha fazla düğüm seçin ve bunları iki liste arasındaki oka tıklayarak Seçilen kuruluş düğümleri listesine taşıyın.  
26. Tamam'a tıklayın.
27. Kaydet'e tıklayın.
    * Bir bağlılık programı şeması için kanalları her değiştirdiğinize Bağlılık şemalarını işle'yi çalıştırmanız gerekir. Bu şekilde, kanallar güncelleştirilmiş bağlılık şemalarını alır.  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
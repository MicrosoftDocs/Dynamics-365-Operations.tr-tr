---
title: Mali boyutlar ve deftere nakletme
description: Hesap planınızı planladığınızda ve ayarladığınızla, bir belgeyi veya günlüğü deftere naklettiğinizde çeşitli bileşenlerin nasıl çalışacağını dikkate almanız gerekir. Bu bileşenler hesap yapıları, gelişmiş kurallar ve bilanço ve sabit boyutları içerir. Bu konu, her bir bileşenin en olduğunu ve bileşenlerin birlikte nasıl çalıştığını açıklar.
author: aprilolson
manager: AnnBe
ms.date: 08/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerChartofAccounts,DimensionDetails
audience: Application User
ms.reviewer: roschlom
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a6179841259186c8438c72bb4a4f9cd2bf5dbaa8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985099"
---
# <a name="financial-dimensions-and-posting"></a>Mali boyutlar ve deftere nakletme 

[!include [banner](../includes/banner.md)]

Hesap planınızı planladığınızda ve ayarladığınızla, bir belgeyi veya günlüğü deftere naklettiğinizde çeşitli bileşenlerin nasıl çalışacağını dikkate almanız gerekir. Bu bileşenler hesap yapıları, gelişmiş kurallar ve bilanço ve sabit boyutları içerir. Bu konu, her bir bileşenin en olduğunu ve bileşenlerin birlikte nasıl çalıştığını açıklar.

## <a name="chart-of-accounts-and-financial-dimension-components"></a>Hesap planı ve mali boyut bileşenleri

Ana hesaplar ve mali boyut değerlerinin geçerli birleşimlerini tanımlamak için kullanılan kural tabanlı, zengin bir sistem. Bu bölüm, her bir bileşenin işlevi hakkında genel bilgi sağlar ve bileşeni nerede bulabileceğinizi açıklar.

### <a name="account-structures"></a>Hesap yapıları

Genel muhasebeyi ayarladığınızda bir hesap yapısı gereklidir. En az bir hesap yapısı tanımlamalı ve etkinleştirmeniz ve daha sonra bunu genel muhasebeye atamanız gerekir. Hesap yapısı ana hesabı içinde bulundurmalıdır. İş için en uygun olan bölüm sırasını tanımlayabilirsiniz. Ana hesap tanımlandıktan sonra, sistem kullanılan hesap yapısını belirleyebilir. Ana hesabı ilk sıraya veya yapını önüne koyarak, değerleri sınırlamaya yardımcı olabilir ve sistemin en son geçerli değeri varsayılan değer olarak kullanmasına yardımcı olabilirsiniz. Hesap yapısında ek olarak 10 adete kadar hesaba sahip olabilirsiniz. Hesap yapısı hangi boyut değerinin diğer değerlerle geçerli birleşimlerde olduğunu tanımlar. Boyut değerlerinin girilmesine gerek olup olmadığını da tanımlar.

### <a name="advanced-rules"></a>Gelişmiş kurallar

Gelmiş kurallar, hesap planını ayarladığınızda isteğe bağlı bir bileşendir. Bir hesap yapısına istediğiniz kadar gelişmiş kural ekleyebilirsiniz. Gelişmiş kurallar genellikle belirli kriterler yerine getirildiğinde izlenmesi gereken ek mali boyutları ele almakta kullanılır. Örneğin, bir Seyahat gider hesabı kullanırsanız, personelin seyahatini gerçekleştirdiği etkinlik gibi ek bilgi izlemek isteyebilirsiniz. Birden fazla gelişmiş kural varsa, kuralların adına dayalı olarak alfabetik sırada uygulanırlar. Bir kuralın eklediği bölüm, yalnızca hesap yapısının bölümlerinden sonra uygulanabilir.

### <a name="balancing-dimension"></a>Bilanço boyutu

İsteğe bağlı olarak bir mali boyut tanımlayabilirsiniz. **Genel muhasebe** sayfasında, dengelenecek mali boyutu tanımlayabilirsiniz. Daha sonra, bu mali boyuta hareketler her deftere nakledildiğinde, sistem otomatik mali boyutu dengede tutmak için olarak girişleri oluşturur ve deftere nakleder.

### <a name="defaultfixed-financial-dimensions-on-the-main-account"></a>Ana hesaptaki varsayılan/sabit mali boyutlar

Varsayılan boyutlar ana kayıtlar gibi çeşitli yerlerden gelir (örneğin müşteri veya satıcı kayıtları), belge başlıkları ve ana hesap gibi. Bu konu, ana hesap üzerindeki tüzel kişiliğe göre varsayılan boyutlara odaklanır. Bir ana hesabın, genel muhasebe için tüm hesap yapılarında kullanılacak her bir mali boyut için **Sabit değil** veya **Sabit** değere sahip olacağını tanımlayabilirsiniz. Bir mali boyut **Sabit değil** ise bir varsayılan değer kullanır ancak bu değer geçersiz kılınabilir. Bu davranış sistemdeki tüm varsayılan değerlere uygulanır; varsayılan değer ana kayıtlardan geliyorsa bile. Bir mali boyut **Sabit** değer olarak ayarlanmışsa, bu değer herhangi bir yerden varsayılan bir değer olarak da gelse, bir kullanıcı tarafından da girilse her zaman uygulanır.

## <a name="order-in-which-default-dimensions-are-applied-during-posting"></a>Deftere nakletme sırasında varsayılan boyutların uygulanma sırası.

Kişiler genellikle çeşitli bileşenlerin hangi sırada çalıştıklarını sorar. Varsayılan boyutların uygulandığı sırayı anlamanız son derece önemlidir çünkü bu davranış, kurulum yapmanız için yaklaşımı etkiler.

> [!NOTE]
> Bu bilgi yalnızca uygulama içerisindeki varsayılan boyutların uygulaması için geçerlidir. Microsoft Excel veya Veri Yönetim Çerçevesi'ni kullanarak içe aktarma yapıyorsanız davranış farklılık gösterir.

### <a name="example-1"></a>Örnek 1

**Hesap yapısı**

| Ana hesap            | İş birimi           | Departman              | Maliyet merkezi             |
|-------------------------|-------------------------|-------------------------|-------------------------|
| Tüm değerlere izin verilir. | Tüm değerlere izin verilir. | Tüm değerlere izin verilir. | Tüm değerlere izin verilir. |

**Ana hesap**

| Ana hesap | Dosya Adı          | Tüzel kişilik | Departman                                 |
|--------------|---------------|--------------|--------------------------------------------|
| 401100       | Ürün Satışları | USMF         | Sabit – 022 Satış ve Pazarlama departmanı |

Aşağıdaki şekil ana hesap 401100 üzerinde ayarlanan sabit varsayılan boyutu gösterir.

[![Varsayılan mali boyutlar](./media/default-dimensions.png)](./media/default-dimensions.png)

Bu son derece basit örnekte, Bölüm boyutunun varsayılan değer **023** (Operasyonlar) kullanmak üzere ayarlandığı bir genel günlük gireceğiz. Bir genel muhasebe hesabı gireceğiz ve deftere nakledeceğiz. Aşağıdaki şekil genel muhasebe defter başlığındaki varsayılan boyutu gösterir.

[![Yevmiye defterleri](./media/general-journal.png)](./media/general-journal.png)

Günlük başlığındaki varsayılan boyut, departman 023'ün satış hesabı satırına varsayılan olarak uygulanmasına neden olur. Aşağıdaki şekil, başlıktaki **023** varsayılan boyut değerinin uygulandığı genel günlük satırını gösterir.

[![Günlük fişi](./media/journal-voucher.png)](./media/journal-voucher.png)

Bununla birlikte, satır deftere nakledildiğinde sabit boyut uygulanır ve satır departman 022'ye nakledilir. Aşağıdaki şekil, sabit boyutun satış hesabına uygulandığı deftere nakledilen fişi gösterir.

[![Fiş hareketleri](./media/voucher-transactions.png)](./media/voucher-transactions.png)

### <a name="example-2"></a>Örnek 2

Örnek ilk örnek ile aynı kurulumu kullanır. Bununla birlikte, ikinci bir bileşen ekleyeceğiz ve dengeleme boyutu olarak Departman boyutunu kullanacağız. Aşağıdaki şekilde **Departman** USMF genel muhasebesi için dengeleme mali boyutu olarak ayarlanır.

[![Genel Muhasebe](./media/ledger.png)](./media/ledger.png)

Aynı günlük başlık kurulumu kullanıldığında ve aynı hareket deftere nakledildiğinde, sabit boyut ilk olarak uygulanır. Daha sonra dengeleme mantığı, her bölümün dengeli bir girişe sahip olduğundan emin olmaya yardımcı olmak için uygulanır. Aşağıdaki örnek sabit boyut uygulandıktan sonraki dengeleme girişini içeren fiş hareketlerini gösterir.

[![Fiş hareketleri](./media/voucher-transactions2.png)](./media/voucher-transactions2.png)

### <a name="example-3"></a>Örnek 3

Bu örnekte, gelişmiş bir kural ekleyeceğiz. Gelişmiş kural, satış hesabı 401100 ve departman 022 (Satış ve Pazarlama) kullanılırsa, sistemin Müşteri adındaki bir ek bölümü izlemesini belirtir.

Bu örnek, sıra sebebiyle önemlidir. Hesap yapısı, an hesap girildikten sonra belirlenir. Hesap yapı kurulumuna başvurursanız, sistem ilgili ana hesabı, iş birimini, departmanı ve maliyet merkezini belirleyebilir. Bu noktada, gelişmiş kural tetiklenmemiştir çünkü sabit boyutlar, varsayılan boyutlar genel fişine deftere nakletme sırasında uygulanana kadar uygulanmaz. Aşağıdaki şekilde Müşteri bölümü mevcut değildir çünkü gelişmiş kural kıstası yerine getirilmemiştir.

[![Genel muhasebe hesabı](./media/drop-down.png)](./media/drop-down.png)

Deftere nakletme başarılı olmaz çünkü sabit boyut işlemin sonunda uygulanmıştır. Boyut doğrulama, Müşteri bölümünün, ana hesap 401100 ve departman 022 olduğunda gerekli olup olmadığını belirler. Doğrulama hatası nedeniyle deftere nakletme gerçekleşemez. Aşağıdaki şekil, boyut doğrulama Müşteri'nin gerekli bir bölüm olduğunu belirledikten sonra beliren mesajı gösterir.

[![İleti ayrıntıları](./media/message.png)](./media/message.png)

Bu örnekte, varsayılan değeri, kural tetiklenecek ve Müşteri bölümünü girebileceğiniz şekilde geçersiz kılmanız gerekir. Ancak, bu çözüm her zaman mümkün değildir ve bazı kullanıcılar deftere nakletme kurallarının farkında bile değildir. Bu nedenle, hesap planınızı ayarladığınızda, uygulanacak varsayılan boyutların sırasını anlamanız önemlidir.

Bu örnekte istediğinizi elde etmek için yapılandırmayı çeşitli şekillerde değiştirebilirsiniz. Örneğin, Müşteri bölümünü yapıda içeren satış hesapları için yeni bir hesap yapısı oluşturabilirsiniz. Mevcut bir hesap yapısına daha fazla satır da ekleyebilir ve ana hesabı ve geçerli bölüm değerlerini belirtebilirsiniz. Daha sonra, ek müşteri yapısında, Müşteri bölümünün mevcut olduğu satış hesapları için ayrı bir hesap yapısı bulundurmayı yararlı bulabilirsiniz.

## <a name="additional-resources"></a>Ek kaynaklar 

Aşağıdaki kaynaklardan bazıları daha önceki bir yazılım sürümüne başvurur. Ancak, varsayılan boyutlar ve pek çok kavram hakkındaki bilgiler önceki sürümle aynıdır ve referanslar halen geçerlidir.

[Birimlerarası muhasebe için dengelenmiş günlükler](example-balanced-journals-interunit-accounting.md)

[Hesap planınızı planlama](plan-chart-of-accounts.md) 

[AX 2012'de hesap planınızı planlamak blog](https://blogs.msdn.microsoft.com/axsa/2014/06/12/planning-your-chart-of-accounts-in-ax-2012-part-1-of-7/) – Bu bağlantı yedi bölümlük bir serinin 1. bölümüne gider.

[Muhasebe dağıtımlarında boyut varsayılanı](https://blogs.msdn.microsoft.com/ax_gfm_framework_team_blog/2013/12/16/dimension-defaulting-in-accounting-distributions-part-1-introduction/)

[Boyutlar çerçevesinde boyutların varsayılanı](https://docs.microsoft.com/archive/blogs/ax_gfm_framework_team_blog/dimension-defaulting-part-1-financial-dimensions-discovery)

---
title: Kıymetleri tedarik yoluyla alma
description: Bu makalede, satınalma siparişlerinden veya satıcı faturalarından otomatik olarak sabit kıymetler oluşturmak veya sabit kıymetler için alım ve alım düzeltme hareketlerini otomatik olarak deftere nakletmek için Sabit kıymetler ile Borç hesapları arasında nasıl tümleştirme oluşturacağı açıklanmaktadır.
author: moaamer
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 3481
ms.assetid: d4e73a3f-633b-48b2-b8db-7a4a59a4d7ec
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac25114fe8036a474d637e9ad9ede5e46b50d92e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891594"
---
# <a name="acquire-assets-through-procurement"></a>Kıymetleri tedarik yoluyla alma

[!include [banner](../includes/banner.md)]

Bu makalede, satınalma siparişlerinden veya satıcı faturalarından otomatik olarak sabit kıymetler oluşturmak veya sabit kıymetler için alım ve alım düzeltme hareketlerini otomatik olarak deftere nakletmek için Sabit kıymetler ile Borç hesapları arasında nasıl tümleştirme oluşturacağı açıklanmaktadır. Bir satınalma satırı bir varlık oluşturacaktır, satınalma satırının miktarı ne olursa olsun. Birden fazla sabit varlık oluşturmanız gerekirse, birden fazla satınalma satırı oluşturmanız gerekir.

 Sabit kıymetlerle ve Borç hesaplarını tümleştirmek için aşağıdaki yöntemler kullanılabilir ve tüm sabit kıymetler için aynı yöntemi kullanmanız gerekir:
-   Satın alma siparişindeki veya satıcı faturadaki satıra sabit kıymet numarası eklemeden önce el ile bir sabit kıymet oluşturmanız gerekir. Satıcı faturasını naklettiğinizde kıymet için deftere otomatik olarak bir alım hareketi nakledilir. Bu, varsayılan yöntemdir.
-   Satın alma siparişindeki veya satıcı faturadaki satıra sabit kıymet numarası eklemeden önce el ile bir sabit kıymet oluşturmanız gerekir. Satıcı faturasını naklettiğinizde, kıymet için deftere alım hareketi nakledilmez.
-   Yeni bir sabit kıymet oluştur seçim kutusu işaretlenmiş bir ürün girişi veya satıcı faturası naklettiğinizde, otomatik olarak yeni bir sabit kıymet oluşturulur. Satıcı faturasını naklettiğinizde kıymet için deftere otomatik olarak bir alım hareketi nakledilir.
-   Yeni bir sabit kıymet oluştur seçim kutusu işaretlenmiş bir ürün girişi veya satıcı faturası naklettiğinizde, otomatik olarak yeni bir sabit kıymet oluşturulur. Satıcı faturasını naklettiğinizde, kıymet için deftere alım hareketi nakledilmez.

Sabit kıymetleri el ile oluşturmayı tercih ediyorsanız ilk iki yöntemden birini seçin ve satın alma siparişine veya satıcı faturasına sabit kıymet numarasını atayın. Daha esnek bir yaklaşımı tercih ediyorsanız son iki yöntemden birini seçin: Satır maddesi ayrıntılarındaki sabit kıymet bilgilerine bağlı olarak kimi zaman sabit kıymetleri el ile oluşturabilir, kimi zaman da otomatik olarak bir sabit kıymet oluşturabilirsiniz. 

Sabit kıymetleri el ile oluştursanız da, daha esnek bir yaklaşım kullansanız da, bir alım hareketinin yalnızca Sabit kıymetlere mi nakledilebileceği yoksa bir satıcı faturası naklettiğinizde de nakledilip nakledilemeyeceğine karar vermeniz gerekir. Bazı organizasyonlar kullanıcıların, el ile günlük girişleri veya teklifleri kullanarak Sabit kıymetlerde alım ve alım hareketlerini el ile oluşturmasını tercih eder. 

Bu makalede her yöntem ayrıntılarıyla ele alınmaktadır.

## <a name="methods-for-manually-creating-fixed-assets"></a> El ile oluşturulan sabit kıymetler için yöntemler
Bu satırlara bir sabit kıymet numarası girilmiş bir satıcı faturasını naklederken, Sabit kıymetler parametreleri sayfasından Satın alma seçeneğinden kıymet alınımına izin ver seçimi yapılırsa alım otomatik olarak nakledilir ve kıymet durumu Açık olarak değişir. 

Bir alım nakledilemiyorsa, bir alım hareketini el ile Sabit kıymetlere girebilir veya aynı anda birden fazla alım hareketi oluşturmak için Sabit kıymetler günlüğündeki bir alım teklifini kullanabilirsiniz.

> [!NOTE]                                                                                                                              
> Sabit kıymetler, belirli bir kullanıcı grubuna alım hareketi nakledilmesini sınırlandıracak şekilde ayarlanmışsa, alım hareketlerini faturalardan nakletmek için o kullanıcı grubunun bir üyesi olmanız gerekir.

## <a name="methods-for-automatically-creating-fixed-assets"></a> Otomatik oluşturulan sabit kıymetler için yöntemler
Bir satır için seçilen yeni bir sabit kıymet seçeneğine sahip bir ürün girişi naklettiğinizde Henüz alınmadı durumuna sahip bir yeni sabit kıymet oluşturulur. Ardından, yeni bir sabit kıymet taşıyan bir satıcı faturası naklederken Sabit kıymetler, Borç hesaplarından kıymet alımlarına izin verecek şekilde ayarlanmışsa ve alım hareketlerini nakledebilen bir kullanıcı grubunun bir üyesiyseniz, yeni kıymet için bir alım hareketi nakledilir ve kıymet durumu Açık olarak değiştirilir. 

Ürün girişini naklettiğinizde satın alma satırında Yeni sabit kıymet? onay kutusu işaretlenmemişse, Sabit kıymetler oluşturma ve alıma izin verecek şekilde ayarlanmışsa, yeni sabit kıymet oluşturulur ve Açık durumuyla alınır. Ürün girişi naklettiğinizde bir kıymet oluşturulmuşsa, bir satıcı faturası naklettiğinizde ek bir kıymet oluşturulmaz.

### <a name="capitalization-threshold"></a>Aktifleştirme eşiği

Kıymetlerin otomatik olarak oluşturulduğu ve alındığı bir yöntem kullandığınızda, sistemi sabit kıymetlerin satınalma tutarının kıymet amortismanı için belirli bir aktifleştirme eşiğini sağladığını doğrulayacak şekilde ayarlayabilirsiniz. Sağlıyorsa, Borç hesaplarından oluşturulduğunda kıymete ait defterlerde Amortisman seçeneği seçilir. 

Aktifleştirme eşiği, kıymetlerin belirtilen bir tutarı karşılamaları durumunda amorti edilip edilmeyeceklerini belirleyen bir nakit tutardır. Örneğin, bir kıymet satın alırsanız ve satınalma tutarı aktifleştirme eşiğinden düşükse, kıymetin amorti edilmesi belirlenmez; satınalma tutarı eşiği sağlar veya geçerse kıymetin amorti edilmesi belirlenir. 

Aktifleştirme eşiğini Sabit kıymet grupları sayfasında ayarlayabilirsiniz.

## <a name="scenario"></a>Senaryo
Aşağıdaki senaryoda Sabit kıymetlerin ve Borç hesaplarının entegre edilmesi için tam bir döngü açıklanmıştır. Bir örnek kurulum gösterilmiş ve ayrıca alım tekliflerinin kullanımı açıklanmıştır. 

Bu senaryoda sistem aşağıdaki gibi ayarlanmıştır:

-   Kıymetler ürün girişi veya satıcı faturası nakli sırasında otomatik olarak oluşturulur ancak Sabit kıymetler, Borç hesaplarından alım hareketlerinin naklini önleyecek şekilde ayarlanmıştır.
-   Hesaplar, madde grupları sayfasındaki Sabit kıymet girişi ve Sabit kıymet çıkışı hesap türleri için Hesap türü alanında belirtilir.
-   Bilgisayarlar grubu (COMP) için aktifleştirme eşiği 1.500'dür.
-   Göreviniz, bir çalışanın kullanacağı yeni bir dizüstü bilgisayar için bir satın alma siparişi girmek, satın alma siparişini deftere nakletmek, sevkiyat memurunun bir ürün girişi naklettiğinden emin olmak, satıcı faturasını nakletmek ve muhasebecinin dizüstü kıymetini Açık durumu ile güncelleştirdiğini doğrulamak şeklindedir.

1.600 maliyetindeki dizüstü bilgisayarın ayrıntılarını girmek için Satın alma emri formunu kullanarak işe başlıyorsunuz. Satın alma emri satırlarının Sabit kıymetler hızlı sekmesinde Yeni sabit kıymet? seçimini yapıyor, sabit kıymet grubu olarak COMP'u seçiyor ve satın alma emrini kaydediyorsunuz. 

Dizüstü bilgisayar alındığında, sevkiyat memuru dizüstü bilgisayarın girişini kaydetmek için bir ürün girişi girer ve nakleder. Dizüstü kıymeti oluşturulur ve Henüz alınmadı durumuna sahip olur. Tutar, aktifleştirme eşiği aşıyor. Bu nedenle, dizüstü bilgisayarı kıymeti için defterler altında Amortisman seçeneği seçilir. Aşağıdaki hareketler oluşur.

| Açıklama                               | Hesap             | Borç    | Alacak   |
|-------------------------------------------|---------------------|----------|----------|
| Satın alma, Ürün girişi satın alma        | Faturalanmamış girişler | 1.600,00 |          |
| Satın alma, Ürün girişi satın alma mahsup | Tahakkuk eden satın almalar   |          | 1.600,00 |

Ardından, dizüstü için satıcı faturası nakledersiniz. Sabit kıymetler, bir satıcı faturası nakledildiğinde kıymet alım hareketinin nakledilmesini önleyecek şekilde ayarlandığından dizüstü bilgisayar durumu değişmez. Satıcı faturası nakledilirken Yeni bir sabit kıymet oluştur seçimi yapılmıştır. Bu nedenle, Sabit kıymet giriş hesabı kullanılmıştır. Bir alım nakledilmemiş olduğundan Sabit kıymet çıkışı hesabı kullanılmamıştır; daha sonra, organizasyonunuzun muhasebecisi alım tekliflerini kullanarak Sabit kıymetlerde bir alım hareketi naklettiğinde kullanılır. 

Aşağıdaki hareketler oluşur.

| Açıklama                               | Hesap             | Borç    | Alacak   |
|-------------------------------------------|---------------------|----------|----------|
| Satın alma, Ürün girişi satın alma mahsup | Tahakkuk eden satın almalar   | 1.600,00 |          |
| Satıcı bakiyesi                            | Borç hesapları    |          | 1.600,00 |
| Satınalma, Sabit kıymet girişi             | Bilgisayar gideri    | 1.600,00 |          |
| Satın alma, Ürün girişi satın alma        | Faturalanmamış girişler |          | 1.600,00 |

Son olarak muhasebeci, Henüz alınmadı durumunda olan tüm sabit kıymetleri inceler. Bu nedenle, yeni dizüstü kıymeti gözden geçirilir. Muhasebeci daha sonra Sabit kıymetler günlük satırlarından Alım teklifi sayfasını açar ve bir fatura içeren ancak hala Henüz alınmadı durumunda olan tüm sabit kıymetler için alım hareketleri oluşturur. Günlük nakledildiğinde, dizüstü kıymetin durumu Açık olarak değiştirilir. Sabit kıymet çıkış hesabı borçlandırılır ve kıymet alı hesabı alacaklandırılır. 

Aşağıda bu senaryonun çeşitlemeleri verilmektedir:

-   Sabit kıymetler, satıcı faturaları nakledildiğinde kıymet alım hareketlerinin nakledilmesine izin verecek şekilde ayarlanmışsa, alım hareketi oluşturulduğundan muhasebecinin Sabit kıymetlerdeki alım tekliflerini kullanmasına gerek olmaz. Aynı zamanda satıcı faturasını naklettiğinizde farklı hesaplar güncelleştirilir. Bilgisayar gideri yerine, Sabit kıymet giriş stok hesabı borçlandırılır ve iki ek hareket oluşur: kıymet alım hesabı alacaklandırılır ve Sabit kıymet çıkış stok hesabı borçlandırılır.
-   Ürün girişi nakledilirken Yeni bir sabit kıymet oluştur seçimi yapılmazsa o anda bir kıymet oluşturulmaz. Satıcı faturasını nakletmeden önce Yeni bir sabit kıymet oluştur seçimini yaparsanız kıymet oluşturulur ve Henüz alınmadı durumuna sahip olur veya satıcı faturaları nakledildiğini alım hareketlerini de naklederseniz Açık durumuna sahip olur.
-   Dizüstü maliyeti 1,600 yerine 1.400 ise, aktifleştirme eşik değerine ulaşılmaz. Bu nedenle, kıymet oluşturulur ve Amortisman seçeneği kaldırılır.
-   Bir fatura defteri kullanılıyorsa fişi almak üzere fatura kaydı nakledildikten sonra Fatura onay günlüğü sayfasını kullanır, satın alma emrini satıcı faturasına bağlar, Yeni bir sabit kıymet oluştur seçimini yapar ve ardından satıcı faturasını nakledersiniz. Alım hareketleri oluşturabilen bir kullanıcı grubunun üyesiyseniz, alım oluşturulur ve kıymetin durumu Açık olur.
-   Yalnızca kısmi bir miktar alınmışsa, kullanıcı grubu kısıtlamaları nedeniyle ilk satıcı faturası için bir kıymet alımı oluşturulmaz. Sipariş edilen miktarı tamamlayan ikinci satıcı faturası için bir alımın nakledilebilmesi için ilk satıcı faturası için bir alım hareketinin girilmiş olması ve alım nakletme iznine sahip bir kullanıcı grubunun bir üyesi olmanız gerekir.


Daha fazla bilgi için bkz: [Sabit kıymet tümleştirmesi](fixed-asset-integration.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

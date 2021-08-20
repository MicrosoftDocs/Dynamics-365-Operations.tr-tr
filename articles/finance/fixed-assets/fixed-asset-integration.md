---
title: Sabit kıymet tümleştirmesi
description: Sabit kıymetler Genel muhasebe, Stok yönetimi, Alacak hesapları ve Borç hesapları ile entegre olabilir. Sabit kıymetleri satınalma emirleri ile entegre olacak biçimde de ayarlayabilirsiniz.
author: ShylaThompson
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3501
ms.assetid: f0639053-d99c-432a-8ead-5c26e0d4eaec
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 290cf4bb28c07dc8ba11250da0fa3af5a8e9cfd7b7c36f688c7f40742dc57b31
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761290"
---
# <a name="fixed-assets-integration"></a>Sabit kıymet tümleştirmesi

[!include [banner](../includes/banner.md)]

Sabit kıymetler Genel muhasebe, Stok yönetimi, Alacak hesapları ve Borç hesapları ile entegre olabilir. Sabit kıymetleri satınalma emirleri ile entegre olacak biçimde de ayarlayabilirsiniz.

## <a name="general-ledger"></a>Genel muhasebe

Genel muhasebede, tüm sabit kıymetlerin değeri genel olarak mali raporlama için gereken birden fazla ana hesapta özetlenir. Ancak, **Sabit kıymetler** sayfasında birçok sabit kıymet kaydı oluşturabilirsiniz. Bu kayıtlar alım fiyatı, amortisman ve değerleme gibi bilgiler içerebilir. Sabit kıymet için deftere her hareket nakledişinizde, ilgili ana hesaplar güncelleştirilir. Sabit kıymetlere ilişkin ana hesaplar her zaman sabit kıymetlerin güncelleştirilmiş değerini gösterir.

**Sabit kıymet deftere nakil profilleri** sayfasında sabit kıymet defter hareketlerinin deftere nakledildiği ana hesapları tanımlarsınız. Her ana hesaba nakledilen sabit kıymet hareketlerinin türlerini de belirtebilirsiniz. Genel muhasebede sabit kıymetler için istediğiniz ayrıntı düzeyine bağlı olarak, sabit kıymetler için çeşitli ana hesap birleşimleri oluşturabilirsiniz. Ana hesaplar hareket türlerine, defterlere ve diğer ana hesaplara dayandırılabilir.

## <a name="inventory-management"></a>Stok Yönetimi
Sabit kıymet stok günlüklerine, tüzel kişiliğin kendi kendine oluşturduğu veya yapılandırdığı sabit kıymetler alımını girebilirsiniz. Ardından, sabit kıymetlere ilişkin stok maddelerini alım veya alımın bir bölümü olarak transfer edebilirsiniz. 

Ayrıca, satınalma siparişlerini kullanarak da varlıklar alabilirsiniz. Satınalma siparişleri sabit kıymet olarak tanımlanan stok maddeleri içerdiğinde, **Sabit kıymet parametreleri** sayfasındaki **Satınalmadan kıymet alımına izin ver** seçeneğinin ayarı, sabit kıymet için bir alımın fatura deftere nakledilirken deftere nakledilip edilmeyeceğini belirler. Bir satınalma satırı, miktarı ne olursa olsun bir sabit kıymet oluşturur. Sabit kıymet alımının stok üzerindeki etkisi tüzel kişiliğin ayarına bağlıdır. 

Bir stok maddesi; stok günlüğü, satınalma siparişi veya alım teklifi üzerinden sabit bir kıymet alımı haline geldiğinde, bir sabit kıymet defteri alım hareketi oluşturulur. Defter alımı türetilmiş defteri içerirse ayrıca türetilmiş defter alım hareketi de oluşturulur. 

Stok yönetimi, **Deftere Nakil** sayfasında ayarlanan deftere nakil kuralları bir alım deftere nakledildiğinde stoktaki düşüşü kontrol eder. Ancak sabit kıymetlerle ilgili faturaları naklettiğinizde stoğu her zaman azaltmazsınız. Bazı durumlarda, sabit kıymetler dahili kullanım için satın alınmış olabilir. Satış departmanı için satın alınan bir dizüstü bilgisayar buna örnek olarak verilebilir. Satınalma siparişleriyle çalışırken, hem yeniden satış hem dahili kullanım için ayarlanmış maddeleri kullanabilirsiniz. 

Madde gruplarında sabit kıymetler için belirli giriş ve çıkış hesaplarını kullanırsanız, hem dahili satın alımlar hem de yeniden satılacak stok için aynı stok maddesini kullanabilirsiniz. 

Dahili kullanıma yönelik sabit kıymetler, bir **Sabit kıymet girişi** hesap türüne sahip olacak şekilde ayarlanır. Bu hesap türü, sabit kıymet girişini izlemek için kullanılır. Bir satıcı faturasını deftere naklettiğinizde, aşağıdaki koşullardan birinin geçerli olması durumunda sabit kıymet giriş hesabını kullanın:

-   Fatura satırının dahili amaçlar için var olan sabit kıymeti içermesi.
-   Deftere nakledilen ürün giriş satırı için **Yeni sabit kıymet?** onay kutusunun seçilmiş olması.
-   Satıcı faturası satırı için **Yeni sabit kıymet oluştur** onay kutusunun seçilmiş olması.

Genel olarak bu hesap bir gider hesabıdır. Madde grubu veya tek tek maddeler için **Sabit kıymet girişi** hesap türünü **Madde grubu** veya **Deftere nakil** sayfasında **Satınalma siparişi** sekmesini kullanarak ayarlayabilirsiniz.

Benzer şekilde, dahili kullanıma yönelik sabit kıymetler, bir **Sabit kıymet çıkışı** hesap türüne sahip olacak şekilde ayarlanabilir. Bu hesap türü, alıcı için sabit kıymet çıkışını izlemek üzere kullanılır. Bir kıymet satınalma siparişi kullanılarak alındığında, sabit kıymet çıkış hesabı sabit kıymet borç hesabını mahsup eder. Kıymet alımı bir satıcı faturasını deftere naklettiğinizde veya Sabit kıymetler günlüğündeki kıymet alımını deftere naklettiğinizde, büyük olasılıkla bir alım teklifi kullanılarak deftere nakledilebilir. Madde grubu veya tek tek maddeler için **Madde grubu** veya **Madde defter nakli** sayfasında **Stok** sekmesini kullanarak **Sabit kıymet çıkışı** hesap türünü ayarlayabilirsiniz. 

Sonuçta, deftere nakil için kullanılan ana hesaplar madde model grubu için belirlenen genel muhasebe tümleştirme seçenekleri tarafından belirlenir. Ayrıca, kullanılan ana hesaplar kıymetin satınalma sipariş satırına atanıp atanmadığına bağlı olarak farklılık gösterir. Hesaplar, her madde grubunun nakil profilinden türetilir. 
**Not:** Ürün girişleri deftere nakledilirken bir stok rezervasyonu varsa satıra bir sabit kıymet atayamaz veya satırdan sabit kıymet oluşturamazsınız. 

Sabit kıymet hareketlerinin deftere nakledildiği hesaplar iki faktöre bağlıdır: Kıymetlerin tüzel kişilik tarafından satın alınması veya oluşturulması ve kıymetin hareket türü. 

Hareket tipi, stok hareketini Sabit kıymetlerdeki deftere nakil profiline bağlar. Sabit kıymetlerdeki deftere nakil profili hangi hesapların güncelleştirileceğini tanımladığından, sabit kıymet hareket tipi seçimi dolaylı olarak aynı zamanda hareketlerin deftere nakledileceği ana hesapların da seçilmesidir. Hem oluşturulan hem de satın alınan sabit kıymetler için, hareket türü genellikle **Alım** veya **Alım düzeltmeleri**'dir.

## <a name="accounts-receivable"></a>Alacak hesapları
Alacak hesaplarını Sabit kıymetlerle tümleştirme, Sabit kıymetler alanında ayarlanan deftere nakil profillerini kullanır. Bu deftere nakil profilleri, müşteri faturası deftere nakledilmeden önce bir müşteri faturası için sabit kıymet, defter ve sabit kıymet hareket türü seçildiğinde etkinleştirilir. Sabit kıymetler Stok yönetiminin parçası olmadığından sabit kıymet sattığınızda **Serbest metin faturası** sayfasını kullanmanız gerekir. 

Defter türetilmiş bir amortisman defteri içeriyorsa, müşteri faturasını deftere naklettiğinizde türetilmiş defter hareketi oluşturulur.

## <a name="accounts-payable"></a>Borç hesapları
Genel olarak sabit kıymetler harici satıcılardan alınır. Satıcı faturalarını naklettiğinizde kıymet alımlarının her zaman nakledilip nakledilmediğini veya kıymet alımlarının yalnızca Sabit kıymetlerden mi nakledilebileceğini belirtmek için **Sabit kıymet parametreleri** sayfasını kullanabilirsiniz. Kıymet alımlarının Borç hesaplarından naklini izin verirseniz bir sabit kıymet alımı için ne zaman bir satıcı faturası nakledilse sabit kıymet hesapları güncelleştirilir. 

Sistem bir fatura nakledildiğinde bir kıymet alımı nakledecek şekilde ayarlanmışsa, hareket çeşitli sabit kıymet hareket tiplerine ait Sabit kıymetler'de ayarlanan deftere nakil profillerine göre nakledilir. Deftere nakil, satıcı faturasını deftere nakletmeden önce **Satınalma siparişi** sayfasında seçilen sabit kıymet, defter ve sabit kıymet hareket türü tarafından denetlenir. 

Defter türetilmiş bir amortisman defteri içeriyorsa, satıcı faturasını deftere naklettiğinizde türetilmiş defter hareketi oluşturulur.

**Satınalma siparişi** sayfasındaki **Satır ayrıntıları** Hızlı Sekmesindeki **Sabit kıymetler** sekmesinde her sipariş satırı için tümleştirme etkinleştirilir. Satıcıya bir sabit kıymet için satınalma siparişi gönderebilirsiniz. Ancak, sabit kıymetler ve ana hesaplar yalnızca, sabit kıymet alındıktan sonra satıcı faturasını deftere nakletmeniz durumunda güncelleştirilir. Satınalma siparişleri yalnızca stok maddelerini içerebileceğinden, sabit kıymet alımının stok üzerindeki etkisi tüzel kişiliğin ayarına bağlıdır.

## <a name="project-management-and-accounting"></a>Proje yönetimi ve muhasebe
Projeyi, projeden etkilenen bir kıymetle ilişkilendirebilirsiniz. Aynı zamanda her aşama, görev veya alt projeyi farklı bir kıymetle ilişkilendirebilirsiniz. Bir kıymet her proje kaydıyla ilişkilendirilebilir. **Projeler** sayfasındaki **Sabit kıymet** numarası alanına sabit kıymet numarasını girdiğinizde ilişkilendirmeyi oluşturursunuz. Proje türü **Dahili** veya **Maliyet projesi** olmalıdır. 

Projelerle ilişkili kıymetlerle ilgili ayrıntıları görüntülemek için **Projeler** sayfasını da kullanabilirsiniz. Sabit kıymet kaydını görüntülemek amacıyla **Sabit kıymetler** sayfasını açmak için **Kurulum** Hızlı Sekmesinde kıymet bağlantısına tıklayın. Ardından, sabit kıymetle ilişkilendirilen projeleri görüntülemek için **Projeler** &gt; **Tüm projeler**'e tıklayın. 

Genel olarak projeler iş, bakım veya kıymet gelişimleriyle ilgili olduğunda sabit kıymetleri projelerle ilişkilendirirsiniz. Proje tamamlandığında, kıymet için otomatik olarak bir değer artırma düzeltmesi oluşturulmaz. Bu nedenle, değer artırma düzeltmesi gerekiyorsa değer artırma düzeltmesini el ile oluşturmanız gerekir. 

Proje ile kıymet arasındaki ilişkilendirmeyi silmek için, **Projeler** sayfasındaki **Sabit kıymet numarası** alanını temizleyin. 

Ayrıca, tahmini bir projenin bir parçası olarak oluşturduğunuz veya ürettiğiniz bir sabit kıymet de atayabilirsiniz. Tahmini projenin sonunda, bir kıymet alım hareketi otomatik olarak deftere nakledebilirsiniz.

Daha fazla bilgi için bkz: [Satınalma aracılığıyla kıymet alma](acquire-assets-procurement.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: "İş şablonları ve konum yönergeleri ile ambar işini denetleyin"
description: "Bu makalede ambar içinde işin nasıl ve nerede gerçekleştirileceğini belirlemek için iş şablonları ve konum yönergelerinin nasıl kullanılacağı açıklanmaktadır."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: f8bcdcf70089aaed06ba0f88cdbec8dfdf9121d1
ms.contentlocale: tr-tr
ms.lasthandoff: 06/13/2017

---

# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>İş şablonları ve konum yönergeleri ile ambar işini denetleyin

[!include[banner](../includes/banner.md)]


Bu makalede ambar içinde işin nasıl ve nerede gerçekleştirileceğini belirlemek için iş şablonları ve konum yönergelerinin nasıl kullanılacağı açıklanmaktadır.

Ambar çalışanlarının bir mobil cihazda aldığı talimatlar, çeşitli ambar işlemleri ve görevlerini tanımlamak üzere Microsoft Dynamics 365 for Finance and Operations'da ayarladığınız iş şablonları ile belirlenir. İş şablonları işin her ambar işlemi için nasıl gerçekleştirildiğini belirler. Bir konum yönergesini iş şablonlarına bağlamakla, işin ambarlardaki belli fiziksel bölgelerde yapılmasının güvenceye alınmasına yardımcı olabilirsiniz.

## <a name="work-templates"></a>İş şablonları
**İş şablonları** sayfası ambarda gerçekleştirilmesi gereken iş operasyonlarını tanımlamanıza olanak sağlar. Genellikle, ambar iş operasyonları bir eylemler çiftinden oluşur: bir ambar çalışanı eldeki stoku bir konumdan çeker ve çekilen stoku başka bir konuma indirir. 

İş şablonları bir başlık ve ilişkili satırlardan oluşur. Her iş şablonu belirli bir *iş sipariş türü*ne yöneliktir. Birçok iş sipariş türü, satınalma ve satış siparişleri gibi kaynak belgeler ile ilişkilendirilir. Ancak, diğer iş siparişi türleri döngü sayımı gibi ayrı ambar işlemlerini ifade eder. *İş havuzu kimliği*'si işi gruplar halinde düzenlemenizi sağlar. 

İş başlığı tanımındaki ayarlar yeni bir iş parçasının ne zaman oluşturulması gerektiğini belirlemek için kullanılabilir. Örneğin, maksimum çekme satırları sayısını ve beklenen maksimum çekme süresini ayarlayabilirsiniz. Sonra, bir satış siparişi çekme işlemi işi bu değerlerden birini aşıyorsa, iş iki iş parçasına bölünür. 

İş satırları işi işlemek için gereken fiziksel görevleri ifade eder. Örneğin, bir çıkış ambarı işleminde, ambar içindeki öğeleri çekmeye yönelik bir iş satırı ve bu öğeleri bir hazırlama alanına indirmeye yönelik başka bir satır olabilir. Sonra yükleme işleminin bir parçası olarak hazırlama alanından öğeleri çekmek için ek bir satır ve öğeleri kamyona indirmek için başka bir satır olabilir. İş şablonu satırlarında bir *yönerge kodu *ayarlayabilirsiniz. Bir yönerge kodu bir konum yönergesine bağlıdır ve böylece ambar işinin ambarda doğru konumda işlendiğine dair güvence vermeye yardımcı olur. 

Belirli iş şablonu kullanıldığında kontrol etmek için bir sorgu ayarlayabilirsiniz. Örneğin, bir sınırlama ayarlayabilirsiniz, böylece yalnızca belirli bir ambardaki iş için belirli bir şablon kullanılabilir. Alternatif olarak, satış menşeine bağlı olarak, giden satış siparişi işleme işi oluşturmak için kullanılan pek çok şablonunuz olabilir. Sistem mevcut iş şablonları değerlendirildiği siparişi belirlemek için **Sıra numarası** alanını kullanır. Bu nedenle, belirli bir iş şablonu için özel bir sorgunuz varsa, buna düşük bir sıra numarası vermelisiniz. Daha sonra bu sorgu diğer, daha genel sorgulardan önce değerlendirilecektir. 

Bir iş işlemini durdurmak veya duraklatmak için, iş satırındaki **İşi durdur** ayarını kullanabilirsiniz. Bu durumda, işi gerçekleştiren çalışandan sonraki iş satırı adımını gerçekleştirmesi istenmeyecektir. Sonraki adıma geçmek için, o çalışan veya başka bir çalışan işi tekrar seçmelidir. Ayrıca iş şablonu satırlarında farklı bir *İş sınıfı kimliği *kullanarak bir iş parçası dahilindeki görevleri ayırabilirsiniz.

## <a name="location-directives"></a>Konum yönergeleri
Konum yönergeleri stok hareketi için çekme ve indirme konumlarını belirlemeye yardımcı olan kurallardır. Örneğin, bir satış siparişi hareketinde, öğelerin nereden çekileceğini ve nereye indirileceğini bir konum yönergesi belirler. Konum yönergeleri bir başlık ve ilişkili satırlardan oluşur ve bunları **Konum yönergeleri** sayfasında oluşturursunuz. 

Başlıkta, her konum yönergesi satış siparişleri, stok yenileme veya hammadde çekme gibi yönergenin kullanılacağı stok hareketinin türünü belirten bir *iş sipariş türü *ile ilişkilendirilmelidir. *İş türü *konum yönergesinin çekme veya indirme işi için veya sayım ya da stok durumu değişiklikleri gibi başka bazı ambar işleri için kullanılıp kullanılmayacağını belirtir. Ayrıca bir *tesis *ve *ambar* belirtmeniz gerekir. Konum yönergesini bir veya birden fazla iş şablonuna bağlamak için başlıkta belirttiğiniz bir *yönerge kodu *kullanılabilir. 

İş şablonlarında olduğu gibi, özel bir konum yönergesinin ne zaman kullanılacağını belirlemek için bir sorgu ayarlayabilirsiniz. Örneğin, e-ticaret bir satış siparişinin menşei olduğunda stokun ambardaki tahsis edilmiş bir alandan ne zaman alınması gerektiğini belirtebilirsiniz. Sistem mevcut konum yönergelerinin değerlendirildiği siparişi belirlemek için **Sıra numarası** alanını kullanır. 

Konum yönergesi satırları konum bulma kurallarının uygulanmasına ek kısıtlamalar getirir. Yönergenin uygulanması gereken minimum miktarı ve maksimum miktarı belirtebilirsiniz ve o yönergenin belli bir stok birimine yönelik olması gerektiğini belirtebilirsiniz. Örneğin, ölçü birimi palet ise, belli bir konuma palet cinsinden öğeler indirilebilir. Miktarın birden çok konum arasında bölünüp bölünemeyeceğini de belirtebilirsiniz. Konum yönergesi başlığı gibi, her konum yönergesi satırının da, satırların değerlendirildiği siparişi belirleyen bir sıra numarası vardır. 

Konum yönergelerinin ek bir ayrıntı düzeyi vardır: *konum yönergesi eylemleri*. Her satır için birden fazla konum yönergesi eylemi tanımlayabilirsiniz. Bir kez daha, bir sıra numarası eylemlerin karar sırasını belirlemek için kullanılır. Bu düzeyde, ambardaki en iyi konumun nasıl bulunacağını tanımlamak için bir sorgu ayarlayabilirsiniz. Ayrıca ideal bir konum bulmak için önceden tanımlanmış **Strateji** ayarlarını da kullanabilirsiniz.

### <a name="example-of-the-use-of-location-directives"></a>Konum yönergelerini kullanım örneği

Bu örnekte, konum yönergesinin, alış noktasında kaydedilen stok öğeleri için bir ambar içinde serbest kapasite bulmasının gerektiği bir satınalma siparişi işlemini ele alacağız. İlk olarak, mevcut eldeki stok ile birleştirerek ambar içinde boş kapasite bulmaya çalışmak istiyoruz. Konsolidasyon mümkün değilse, bu durumda boş bir yer bulmak istiyoruz. 

Bu senaryo için iki konum yönergesi eylemi tanımlamamız gerek. Sıradaki ilk eylemin **Konsolide Et** stratejisini ve ikinci eylemin **Gelen iş olmayan boş yer** stratejisini kullanması gerekir. Biz bir taşma senaryosunu idare etmek için üçüncü bir eylem tanımlamadığımız takdirde, ambarda daha fazla kapasite olmadığında iki sonucun meydana gelmesi olasıdır: iş hiçbir konum tanımlanmasa da oluşturulabilir veya iş oluşturma işlemi başarısız olabilir. Sonuç **Konum yönergesi hataları** sayfasındaki ayara göre belirlenir; burada her bir iş siparişi türü için **Konum yönergesi hatasında işi durdur** seçeneğini seçip seçmemeye karar verebilirsiniz.





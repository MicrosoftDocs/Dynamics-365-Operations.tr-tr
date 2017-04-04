---
title: Kaynak yetenekleri
description: "Bu makale, kaynak yetenekleri hakkında bilgi sağlar. Yetenek, bir operasyon kaynağının belirli bir etkinliği gerçekleştirebilme becerisidir. Makale, yeterlilik düzeyi ve öncelik gibi yeteneklerin ve ilgili kavramların bir etkinlik için uygun kaynakların seçilmesinde nasıl kullanıldığını açıklar."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WrkCtrCapability, WrkCtrTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 29961
ms.assetid: 30e38233-2a64-4070-911f-8ffd78dd8281
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 4463ca8e11115eb83323716faa4ed6b38937a3e4
ms.lasthandoff: 03/31/2017


---

# <a name="resource-capabilities"></a>Kaynak yetenekleri

Bu makale, kaynak yetenekleri hakkında bilgi sağlar. Yetenek, bir operasyon kaynağının belirli bir etkinliği gerçekleştirebilme becerisidir. Makale, yeterlilik düzeyi ve öncelik gibi yeteneklerin ve ilgili kavramların bir etkinlik için uygun kaynakların seçilmesinde nasıl kullanıldığını açıklar.

Yetenek, bir operasyon kaynağının belirli bir etkinliği gerçekleştirebilme becerisidir. İşlem kaynağının atanmış birden fazla yeteneği olabilir ve bir yetenek için birden fazla kaynak atanabilir. Yetenek atamasında bir başlangıç tarihi ve bitiş tarihi tanımlayarak yetenekleri geçici olarak operasyon kaynaklarına atayabilirsiniz. Kaynağın yeteneği sona erdiğinde, bir proje ya da bu yeteneği gerektiren bir üretim için kaynak zamanlanamaz. Süresi dolmuş bir yetenek yenilenebilir. Bunlar bir rota ilişkisi veya bir üretim rotası etkin üretim emrinin parçası olmaması koşuluyla, yetenekleri silebilirsiniz. Genel olarak, yetenekleri silerken dikkatli olun. Bunun yerine, yeteneği olan kaynakların sona erme tarihini ayarlamayı göz önünde bulundurun. Yetenekler tüm operasyon kaynağı türlerine atanabilir: araç, satıcı, makine, konum, tesisi veya insan kaynakları.

## <a name="level"></a>Raf
Birden fazla kaynak genellikle aynı işlevsel yeteneğine sahiptir, ancak farklı düzeylerde yeterliliği vardır (örneğin, gücü, işlemci hızı veya doğruluk). Bu nedenle, bir yeteneği bir kaynağa atadığınızda **düzey** değeri belirtebilirsiniz. Düzey bir basit sayısal değerdir. Bir yeteneğin bir üretim rotası için bir kaynak gereksinimi olduğunu belirtirseniz, bu yetenek için ayrıca bir **gereken en düşük düzey** değeri belirtebilirsiniz. Zamanlama altyapısı sonra kaynak gereksiniminde belirtilen minimum düzeye eşit veya aşan bir düzeyde olan gerekli yeteneği olan kaynakları seçer.

## <a name="priority"></a>Öncelik
Aynı yetenekleri olan işlem kaynaklarına bir öncelik atanabilir. Sonra birden fazla kaynak gerekli düzeyde zamanlama gereksinimlerini karşılamak yeteneklere sahiptir ve ücretsiz kapasitesine sahip, zamanlama altyapısı bu kaynakları arasında seçebilirsiniz. Varsa **öncelik** seçilir **birincil kaynak seçim** alanına **zamanlaması parametrelerini** sayfası, en yüksek önceliğe sahip kaynak (en düşük sayısal değer **öncelik** alan) seçili planlama sırasında ilk.

## <a name="resource-requirements"></a>Kaynak gereksinimleri
Üretim rotası için kaynak gereksinimleri tanımladığınızda, bir veya daha fazla yetenekleri gereksinim olarak belirtebilirsiniz. Üretim planlama sırasında kaynak gereksinimleri Rota operasyonu üzerinde tanımlanan özellikler kaynaklar için tanımlanan özellikler ile eşleştirilir. Gereksinimleri karşılayan yetenekleri olan kaynaklar seçilir. Birden fazla kaynak (örneğin, gücü, işlemci hızı veya doğruluk) farklı uzmanlıkları ama aynı işlev yeteneği varsa, birden çok yetenekleri tanımlayabilir veya kaynağın yeteneği nitelemek için yetenek düzeyi kullanabilirsiniz. Aşağıda bir örnek verilmiştir:

-   Bir rota üzerinde drilling işlem süresi saat başına 10 birim için ayarlanır, ancak gereksinim Drilling olarak tanımlanır.
-   İki Delme makineleri, M1 ve M2 var.
-   Drilling yeteneği, kaynaklar, makine M1 ve M2 makine için atanır.
-   M1 makine saat başına iki birim inebilir ve saat başına 11 birim M2 makine inebilir.

Bu örnekte, (Drilling) temel yeteneği gereksinimi karşıladığı için her iki makine zamanlama altyapısı tarafından seçilebilir. Ancak, M1 makine yalnızca iki birim saat başına inebilir. Bu oran çok rotasında belirtilen saat başına 10 birimden daha az olduğu için seçili ise M1 makine üretim sorunlarına neden olur. Yerine M2 makine seçili olduğundan emin olun ve bu sorunu çözmek için iki yol vardır:

-   İki ayrı yetenekleri oluşturun: düşük hızlı Delme ve yüksek hızlı Delme. Düşük hızlı bir işlem süresi için bir ila dokuz saat başına birim sayısıyla, inme tanımlayın. Yüksek hızlı bir işlem süresi için 10 ila 19 saat başına birim sayısıyla, inme tanımlayın. Sonra düşük hızlı drilling yeteneği M1 makine atamak ve yüksek hızlı drilling yeteneği M2 makine atayabilirsiniz. Son olarak, yol üzerinde kaynak becerisi gereksinimi yüksek hızlı Delme için değiştirin. Zamanlama altyapısı sonra doğru makine (M2) seçer.
-   Drilling makineleri için atanan Drilling yeteneği nitelemek için yetenek düzeyi kullanın. M1 makine 2.0 bir düzeyde Drilling kapasitesine sahip ve M2 makine 11.0 bir düzeyde Drilling yeteneği olduğunu belirtin. Sonra 10.0 rotadaki Drilling yeteneği ihtiyaç için gerekli olan minimum düzeye olduğunu belirtin. Zamanlama altyapısı sadece M2 makine kaynak gereksinimlerini karşılayan olduğunu belirleyecektir.

## <a name="competencies-for-human-resources"></a>İnsan kaynakları için yetkinlikler
İnsan Kaynakları çalışanlarının bağlı **İnsan Kaynakları** işlem kaynakları türüne sahip olduğunuzda üretim rotası için kaynak gereksinimleri tanımladığınızda, ayrıca çalışanların yetkinliklerinden yararlanabilirsiniz. Diğer bir deyişle, gereksinimleri için özel nitelikler, kurslar, sertifikaları veya başlık belirtebilirsiniz. Zamanlama altyapısı sonra işçilere bağlı kaynakları seçer ve seçimi, bu çalışanların yetkinlikleri üzerinde temel alır. Yetkinlikler İnsan Kaynakları'nda kurulur, **kaynak yetenekleri** sayfasında değil. Becerileri, kurslar, sertifikaları veya başlık kaynak gereksinimleri tanımladığınızda, İnsan Kaynakları işlevselliğini kullanmak gerekir ve her kaynak bağlantı **İnsan Kaynakları** için karşılık gelen bir alt türü. İnsan Kaynakları işlevini kullanmıyorsanız, temel özellikleri tanımlayabilirsiniz **kaynak yetenekleri** benzer veya İnsan Kaynakları'ndan yetkinlikleri yinelenen sayfa. Ancak, **kaynak yetenekleri** sayfası nitelikleri, kurslar, sertifikaları veya başlıklar sağlamak için gerekli işlevselliği içermez.



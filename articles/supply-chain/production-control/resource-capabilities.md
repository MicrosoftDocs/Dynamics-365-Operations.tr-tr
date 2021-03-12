---
title: Kaynak yetenekleri
description: Bu makale, kaynak yetenekleri hakkında bilgi sağlar. Yetenek, bir operasyon kaynağının belirli bir etkinliği gerçekleştirebilme becerisidir. Makale, yeterlilik düzeyi ve öncelik gibi yeteneklerin ve ilgili kavramların bir etkinlik için uygun kaynakların seçilmesinde nasıl kullanıldığını açıklar.
author: sorenva
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrCapability, WrkCtrTable, WrkCtrCapRes, WrkCtrApplicableResources
audience: Application User
ms.reviewer: kamaybac
ms.custom: 29961
ms.assetid: 30e38233-2a64-4070-911f-8ffd78dd8281
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 445ef49440fa789bee60e508698abed755c54795
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986562"
---
# <a name="resource-capabilities"></a>Kaynak yetenekleri

[!include [banner](../includes/banner.md)]

Bu makale, kaynak yetenekleri hakkında bilgi sağlar. Yetenek, bir operasyon kaynağının belirli bir etkinliği gerçekleştirebilme becerisidir. Makale, yeterlilik düzeyi ve öncelik gibi yeteneklerin ve ilgili kavramların bir etkinlik için uygun kaynakların seçilmesinde nasıl kullanıldığını açıklar.

Yetenek, bir operasyon kaynağının belirli bir etkinliği gerçekleştirebilme becerisidir. İşlem kaynağının atanmış birden fazla yeteneği olabilir ve bir yetenek için birden fazla kaynak atanabilir. Yetenek atamasında bir başlangıç tarihi ve bitiş tarihi tanımlayarak yetenekleri geçici olarak operasyon kaynaklarına atayabilirsiniz. Kaynağın yeteneği sona erdiğinde, bir proje ya da bu yeteneği gerektiren bir üretim için kaynak zamanlanamaz. Süresi dolmuş bir yetenek yenilenebilir. Bunlar bir rota ilişkisi veya bir üretim rotası etkin üretim emrinin parçası olmaması koşuluyla, yetenekleri silebilirsiniz. Genel olarak, yetenekleri silerken dikkatli olun. Bunun yerine, yeteneği olan kaynakların sona erme tarihini ayarlamayı göz önünde bulundurun. Yetenekler tüm operasyon kaynağı türlerine atanabilir: araç, satıcı, makine, konum, tesisi veya insan kaynakları.

## <a name="level"></a>Raf
Birden fazla kaynak genellikle aynı işlevsel yeteneğine sahiptir, ancak farklı düzeylerde yeterliliği vardır (örneğin, gücü, işlemci hızı veya doğruluk). Bu nedenle, bir yeteneği bir kaynağa atadığınızda **düzey** değeri belirtebilirsiniz. Düzey bir basit sayısal değerdir. Bir yeteneğin bir üretim rotası için bir kaynak gereksinimi olduğunu belirtirseniz, bu yetenek için ayrıca bir **gereken en düşük düzey** değeri belirtebilirsiniz. Zamanlama altyapısı sonra kaynak gereksiniminde belirtilen minimum düzeye eşit veya aşan bir düzeyde olan gerekli yeteneği olan kaynakları seçer.

## <a name="priority"></a>Öncelik
Aynı yetenekleri olan işlem kaynaklarına bir öncelik atanabilir. Ardından, birden fazla kaynak zamanlama gereksinimlerini karşılama yeteneklerine gerekli düzeyde sahipse ve serbest kapasitesi varsa, zamanlama altyapısı bu kaynaklar arasından seçilebilir. **Planlama parametreleri** sayfasındaki **Birincil kaynak seçimi** alanında **Öncelik** seçilirse, en yüksek önceliğe sahip kaynak (**Öncelik** alanındaki en düşük sayısal değer) planlama sırasında ilk olarak seçilir.

## <a name="resource-requirements"></a>Kaynak gereksinimleri
Üretim rotası için kaynak gereksinimleri tanımladığınızda, bir veya daha fazla yetenekleri gereksinim olarak belirtebilirsiniz. Üretim planlama sırasında kaynak gereksinimleri Rota operasyonu üzerinde tanımlanan özellikler kaynaklar için tanımlanan özellikler ile eşleştirilir. Gereksinimleri karşılayan yetenekleri olan kaynaklar seçilir. Birden fazla kaynak (örneğin, gücü, işlemci hızı veya doğruluk) farklı uzmanlıkları ama aynı işlev yeteneği varsa, birden çok yetenekleri tanımlayabilir veya kaynağın yeteneği nitelemek için yetenek düzeyi kullanabilirsiniz. Aşağıda bir örnek verilmiştir:

-   Bir rota üzerinde drilling işlem süresi saat başına 10 birim için ayarlanır, ancak gereksinim Drilling olarak tanımlanır.
-   İki Delme makineleri, M1 ve M2 var.
-   Drilling yeteneği, kaynaklar, makine M1 ve M2 makine için atanır.
-   M1 makine saat başına iki birim inebilir ve saat başına 11 birim M2 makine inebilir.

Bu örnekte, (Drilling) temel yeteneği gereksinimi karşıladığı için her iki makine zamanlama altyapısı tarafından seçilebilir. Ancak, M1 makine yalnızca iki birim saat başına inebilir. Bu oran çok rotasında belirtilen saat başına 10 birimden daha az olduğu için seçili ise M1 makine üretim sorunlarına neden olur. Yerine M2 makine seçili olduğundan emin olun ve bu sorunu çözmek için iki yol vardır:

-   İki ayrı yetenekleri oluşturun: düşük hızlı Delme ve yüksek hızlı Delme. Düşük hızlı bir işlem süresi için bir ila dokuz saat başına birim sayısıyla, inme tanımlayın. Yüksek hızlı bir işlem süresi için 10 ila 19 saat başına birim sayısıyla, inme tanımlayın. Sonra M1 makinesini Düşük hızlı delme yeteneğine ve M2 makinesini Yüksek hızlı delme yeteneğine atayın. Son olarak, rotadaki kaynak becerisi gereksinimini Yüksek hızlı delme olarak değiştirin. Zamanlama altyapısı sonra doğru makine (M2) seçer.
-   Drilling makineleri için atanan Drilling yeteneği nitelemek için yetenek düzeyi kullanın. Makine M1'in 2,0 düzeyinde delme yeteneğine sahip olduğunu ve makine M2'nin 11,0 düzeyinde Delme yeteneğine sahip olduğunu belirtin. Ardından rotadaki Delme yeteneği gereksinimi için gerekli olan minimum düzeyin 10,0 olduğunu belirtin. Zamanlama altyapısı sadece M2 makine kaynak gereksinimlerini karşılayan olduğunu belirleyecektir.

## <a name="competencies-for-human-resources"></a>İnsan kaynakları için yetkinlikler
İnsan Kaynakları çalışanlarının bağlı **İnsan Kaynakları** işlem kaynakları türüne sahip olduğunuzda üretim rotası için kaynak gereksinimleri tanımladığınızda, ayrıca çalışanların yetkinliklerinden yararlanabilirsiniz. Diğer bir deyişle, gereksinimleri için özel nitelikler, kurslar, sertifikaları veya başlık belirtebilirsiniz. Zamanlama altyapısı sonra işçilere bağlı kaynakları seçer ve seçimi, bu çalışanların yetkinlikleri üzerinde temel alır. Yetkinlikler İnsan Kaynakları'nda kurulur, **kaynak yetenekleri** sayfasında değil. Becerileri, kursları, sertifikaları veya başlıkları kaynak gereksinimleri olarak tanımladığınızda, İnsan kaynakları işlevini kullanmanız ve **İnsan Kaynakları** türündeki her kaynağı karşılık gelen bir çalışana bağlamanız gerekir. İnsan Kaynakları işlevini kullanmıyorsanız, yetenekleri İnsan kaynaklarına benzeyen veya yetenekleri buradan kopyalayan **Kaynak yetenekleri** sayfasında tanımlayabilirsiniz. Ancak, **kaynak yetenekleri** sayfası nitelikleri, kurslar, sertifikaları veya başlıklar sağlamak için gerekli işlevselliği içermez.




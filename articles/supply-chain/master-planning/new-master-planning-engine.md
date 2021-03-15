---
title: Master planlama için Planlama İyileştirmesi'ne geçiş
description: Bu konu, yeni master planlama altyapısı, Planlama İyileştirmesi ve var olan altyapıdan geçiş hakkında bilgi sağlar.
author: ChristianRytt
manager: tfehr
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: crytt
ms.search.validFrom: 2020-11-05
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8a55958a4b9573a7c3527d3d97cbcb818457b995
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/15/2021
ms.locfileid: "5008002"
---
# <a name="migration-to-planning-optimization-for-master-planning"></a>Master planlama için Planlama İyileştirmesi'ne geçiş

[!include [banner](../includes/banner.md)]

Yerleşik master planlama altyapısının devre dışı (devre dışı) bırakılması planlanmaktadır. Yerini, Microsoft Dynamics 365 Supply Chain Management için Planlama İyileştirmesi Eklentisi alacaktır. Bu konu, yeni ve var olan dağıtımlar üzerindeki etkisi hakkında bilgi sağlar. Gerekli eylemler hakkında bilgi içerir.

Planlama İyileştirmesi, master planlama hesaplamalarının Supply Chain Management ve Azure SQL veritabanı dışında gerçekleşmesini sağlar. Planlama İyileştirmesi ile ilişkili avantajlar arasında master planlama çalışmaları sırasında artan performans ve SQL veritabanı üzerinde en az etki vardır. Hızlı planlama çalıştırmaları, ofis saatlerinde de yapılabildiği için planlayıcılar, talep ve parametre değişikliklerine hemen tepki verebilir.

Planlama İyileştirmesi hakkında daha fazla bilgi için bkz. [Planlama İyileştirmesi'ne genel bakış](planning-optimization/planning-optimization-overview.md).

## <a name="obsolescence-of-the-existing-master-planning-engine"></a>Var olan master planlama altyapısının kullanım dışı bırakılması

Microsoft, yerleşik planlama altyapısını yerini Planlama İyileştirmesi alacak şekilde kullanım dışı bırakma sürecindedir. Bu değişiklik tüm bulut ortamlarını etkiler. Şirket içi kurulumlar etkilenmez. 10.0.16 ve sonraki sürümlerde, yerleşik master planlamayı planlı üretim emirleri oluşturmadan çalıştırıyorsanız bir hata iletisi alırsınız. Ancak, master planlama çalıştırması hata iletisine rağmen başarıyla tamamlanır.

Yerleşik planlama altyapısının kullanım dışı bırakılması hakkında daha fazla bilgi için [Dynamics 365 Supply Chain Management'ta kaldırılan ve kullanım dışı bırakılan özellikler](../get-started/removed-deprecated-features-scm-updates.md) bölümündeki duyurulara bakın.

## <a name="migration-messages-and-exceptions"></a>Geçiş, iletiler ve özel durumlar

Planlı üretim emirleri olmadan yerleşik master planlama altyapısını çalıştıran mevcut ortamların sahipleri, özel durum işlemiyle ilgili ayrıntıların bulunduğu bir posta alacaktır. Planlamayı En İyi Duruma Getirme için geçişi değerlendirmek ve planlamak üzere bir iş ortağı ile çalışmanız önerilir.

Belirtildiği gibi 10.0.16 ve sonraki sürümlerde, yerleşik master planlamayı planlı üretim emirleri oluşturmadan çalıştırıyorsanız bir hata iletisi alırsınız. Bu hata iletisi, geçişle ilgili yönergeler ve özel bir özel durum istemek için yönergeler içerir.

### <a name="new-deployments"></a>Yeni dağıtımlar

Planlama İyileştirmesi, buluttaki tüm yeni dağıtımlar için varsayılan master planlama altyapısı olarak kabul edilmelidir. Genel olarak, master planlama sırasında planlı üretim emirleri oluşturmayan tüm yeni dağıtımlar için Planlamayı En İyi Duruma Getirme işlevi kullanılmalıdır. Yeni bir dağıtım, Planlama İyileştirmesi'nin şu anda desteklemediği işlevselliğe bağlıysa, yerleşik master planlama altyapısını kullanmaya devam etmek için bir özel durum isteyebilirsiniz.

### <a name="existing-deployments"></a>Var olan dağıtımlar

Master planlamaya bağlı olan bulut tabanlı dağıtımların sahipleri, Planlama İyileştirmesi'ne geçiş yapmayı planlamalıdır. Uygulamanız, Planlama İyileştirmesi'nin şu anda desteklemediği işlevselliğe bağlıysa, yerleşik master planlama altyapısını kullanmaya devam etmek için bir özel durum isteyebilirsiniz.

Şu anda kullanım dışı bırakılacak master planlama işlemlerini kullanan ortamlar için Microsoft, ortam yöneticisine bir e-posta gönderir. Bu e-posta, geçiş yapmak veya bir özel durum istemek için gereken eylemler hakkında bilgi sağlar.

## <a name="the-exception-process"></a>Özel durum süreci

İş süreçleriniz büyük ölçüde Planlama İyileştirmesi'nde şu anda uygulanmayan en az bir özelliğe bağlı olduğundan yerleşik master planlama altyapısını kullanmaya devam etmek zorundaysanız bir özel durum isteyebilirsiniz. Kullanılabilir özelliklerin listesi için [Planlama İyileştirmesi uyum analizi](planning-optimization/planning-optimization-fit-analysis.md)bölümüne bakın.

Şu anda, Planlama İyileştirmesi geçişi için özel durumlar yalnızca master planlama işleminiz üretim içermiyorsa (diğer bir deyişle, master planlama tarafından oluşturulan planlı üretim emirleri) ve 10.0.15 sürümü sonrasında yerleşik master planlama altyapısına ihtiyaç duyuyorsanız yapılmalıdır.

Gerekli özellikler kullanıma sunulduktan sonra, Microsoft özel durum süresi dolana kadar bir yetkisiz kullanım süresi sağlar. Gerekli özellikler kullanılabilir hale geldiğinde ve yetkisiz kullanım süresi başladığında ortam yöneticisi bilgilendirilecektir.

> [!NOTE]
> Sadece üretim ortamları için bir özel durum isteyebilirsiniz, korumalı alan ortamları için değil. Hizmet olarak altyapı (IaaS) korumalı alan ortamında bir Planlama İyileştirmesi özel durum hatasını devre dışı bırakmanız gerekiyorsa [Korumalı alan ortamları](#faq-sandbox) bölümünde sağlanan SQL sorgusunu çalıştırın.

## <a name="frequently-asked-questions"></a>Sık sorulan sorular

### <a name="sandbox-environments"></a><a name="faq-sandbox"></a>Korumalı alan ortamları

Korumalı alan ortamımda yerleşik master planlamayı kullanabilir miyim? Özel duruma ihtiyacım var mı?

**Yanıt:** Planlama İyileştirmesi özel durum hatası yerleşik master planlama altyapısının başarılı çalışmasını engellemediği için özel durumlar normalde korumalı alan ortamları için geçerli değildir. Ancak, hata iletisi sizi rahatsız ederse veritabanınızda aşağıdaki sorguyu çalıştırarak bir IaaS (Service Fabric değil) korumalı alan ortamında, iletiyi devre dışı kullanabilirsiniz:

```sql
-- Insert or update an enabled flight:
DECLARE @flightName NVARCHAR(100) = 'ReqPlanningOptimizationExceptionToggle';
IF NOT EXISTS (SELECT TOP 1 1 FROM SysFlighting WHERE flightName = @flightName)
    INSERT INTO SYSFLIGHTING(FLIGHTNAME,ENABLED, FLIGHTSERVICEID,PARTITION)
    SELECT @flightName, 1, 12719367,RECID FROM DBO.[PARTITIONS];
ELSE
    UPDATE SysFlighting SET enabled = 1, flightServiceId = 12719367 WHERE flightName = @flightName;
```

### <a name="on-premises-environments"></a>Şirket içi ortamlar

Ortamım şirket içinde. Özel duruma ihtiyacım var mı?

**Yanıt:** Hayır. Şirket içi ortamlar için bir özel durum gerekmez. Yerleşik master planlamayı kullanmaya devam edebilirsiniz. Herhangi bir işlem gerekirse ortam yöneticiniz bilgilendirilecektir.

### <a name="production-scenarios"></a>Üretim senaryoları

Planlı üretim emirleri kullanıyoruz ancak 10.0.16 sürümüne yükselttiğimizde ne olacağı konusunda endişeliyim. Harekete geçmeli miyim?

**Yanıt:** Endişelenmeyin. 10.0.16 sürümünde yerleşik master planlamayı kullanmaya devam edebilirsiniz. Ancak Planlama İyileştirmesi'ne geçişin geçerli işlevsellikle başlayıp başlamayacağı konusunu değerlendirmenizi öneririz. Ayrıca, yeni işlevler hakkında bilgi edinmenizi öneririz.

### <a name="email-from-microsoft"></a>Microsoft'tan e-posta

Ortam yöneticimiz Microsoft'tan bir e-posta aldı. Bu e-posta, Planlama İyileştirmesi'ne geçiş yapmamız veya bir özel durum istememiz gerektiğini belirtiyor. Herhangi bir işlem yapmam gerekiyor mu?

**Yanıt:** Evet. E-postadaki yönergeleri izlemediğiniz sürece ortamınız etkilenir. Belirtilen tarihe kadar Planlama İyileştirmesi'ne geçiş yapabilir veya e-postadaki bağlantıyı kullanarak bir özel durum isteyebilirsiniz. Bu bağlantı bir anket açar. Bu anketi tamamladıktan ve gönderdikten sonra, e-posta yoluyla bir yanıt alacaksınız. Bu işlem el ile olmasına rağmen, Microsoft anket formunun gönderilmesinden sonraki bir hafta içinde yanıtlamaya çalışır.

### <a name="error-messages"></a>Hata iletileri

10.0.16 veya sonraki bir sürüm kullanıyorum ve master planlamayı çalıştırdığımda aşağıdaki hata iletisini alıyorum. Master planlama engellendi mi?

> Bu hata iletisini, yerleşik master planlama altyapısı Planlama İyileştirmesi tarafından desteklenen senaryolar için kullanıldığı için alırsınız. Geçerli yerleşik master planlama kullanım dışı bırakılacağından şimdi Planlama İyileştirmesi'ne geçiş yapmalısınız. Bu master planlama çalıştırmasının başarıyla tamamladığını unutmayın.
>
> Geçişinizin beklemedeki özelliklere güçlü bağımlılıkları olması durumunda, yerleşik master planlama altyapısının sürekli kullanımı için bir özel durum isteyebilirsiniz.
>
> Başlamak için lütfen aşağıdaki anketi doldurun ve ilgili istek durumunda Planlama İyileştirmesi'ne geçişle ilgili özel bir durum isteyin.

**Yanıt:** Hayır, master planlama engellenmedi. Master planlama çalıştırmanız başarıyla tamamlandı ve sonucu her zamanki gibi kullanabilirsiniz. Ancak, gelecekteki master planlama çalıştırmaları sırasında bu hata iletisini almaktan kaçınmak için hemen Planlama İyileştirmesi'ne geçiş yapmalı veya hata iletisindeki bağlantıyı kullanarak bir özel durum istemeniz gerekir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
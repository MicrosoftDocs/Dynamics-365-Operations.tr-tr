---
title: Dynamics 365 Human Resources altyapı birleştirme hakkında genel bakış
description: Bu makalede, Microsoft Dynamics 365 Human Resources altyapı birleştirmesi açıklanmaktadır.
author: twheeloc
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e68b28bfde35b51605aa0b653265da6261b69a90
ms.sourcegitcommit: 68efa7b89273d04484566cbe14d3533a8fd4ee53
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/02/2022
ms.locfileid: "9819255"
---
# <a name="dynamics-365-human-resources-infrastructure-merge"></a>Dynamics 365 Human Resources altyapı birleştirmesi 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="dynamics-human-resources-365"></a>Dynamics Human Resources 365

Microsoft Dynamics 365 Human Resources, İK ekiplerinin kurumsal çevikliği artırmasına, personel deneyimini dönüştürmelerine ve İK programlarını optimize ederek çalışanların ve işletmenin gelişebileceği bir iş yeri oluşturmasına yardımcı olan araçlar sağlamaktadır. Dynamics 365 Human Resources hakkında daha fazla bilgi edinmek için bkz. [Dynamics 365 Human Resources](https://dynamics.microsoft.com/human-resources/overview/).

- **Personel deneyimini dönüştürün.** Bağlılığı ve büyümeyi teşvik eden bağlantılı self servis deneyimler aracılığıyla yöneticileri ve personeli güçlendirerek en iyi performans gösterenleri elde tutun.
- **İK programlarını iyileştirin.** Operasyon maliyetlerini azaltın ve insanlar merkezli izin ve devamsızlık, zaman, kazanç ve ücret yönetimi programları oluşturmaya yardımcı olun.
- **Kurumsal çevikliği artırın.** Kişi verilerini merkezileştirmek ve Dynamics 365 Human Resources'ı kolayca genişletmek için Dataverse ve Microsoft Power Platform kullanarak İK'nın işletmenin ihtiyaç duyduğu beceriyle çalışmasını sağlayın.
- **İşgücü hakkındaki öngörüleri keşfedin.** Herhangi bir cihazda erişilebilen zengin panolarda kişi verilerini analiz etme ve görselleştirme özelliği ile veri odaklı kararlar verin.

## <a name="human-resources-infrastructure-merge"></a>Human Resources altyapısını birleştirme

Dynamics 365 Human Resources, şu anda Dynamics 365 Finance veya Dynamics 365 Supply Chain Management gibi finans ve operasyon uygulamaları dışında farklı altyapılar kullanan bağımsız bir uygulamadır. Altyapı birleştirme, Dynamics 365 Human Resources'ı diğer finans ve operasyon uygulamalarıyla aynı altyapıya getirecektir.

Human Resources altyapı birleştirme hakkında daha fazla bilgi edinmek için bkz. [HR tekliflerinin birleştirmesi](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers/). Sık sorulan soruların yanıtları için, bkz. [Human Resource altyapı birleştirmesi hakkında SSS](./hr-infrastructure-merge-faq.md).

## <a name="customer-migration-vs-customer-merge"></a>Müşteri geçişi ve müşteri birleştirme karşılaştırması

Altyapı birleştirmesinin bir parçası olarak Human Resources uygulamasının tüm özellikleri, finans ve operasyonlar ortamlarında kullanılabilir olmuştur. Müşteriler, Microsoft Dynamics Lifecycle Services'ta bulunan geçiş aracını kullanarak Human Resources ortamlarını geçirebilirler. Ayrıca isteğe bağlı olarak, varolan finans ve operasyonlar ortamıyla veri birleştirebilirler. 

Müşteri geçişi ve müşteri birleştirme aşağıdaki şekilde farklılık gösterir:

- **Müşteri geçişi** – Otomatik geçiş aracı, Human Resources alt yapısının bir "lift-and-shift geçiş" (taşıma) işlemini finans ve operasyonlar altyapısına uygulamak amacıyla kullanılır. Sonuç, müşterinin Human Resources veritabanını kullanan yeni bir finans ve operasyonlar ortamıdır. 
- **Müşteri birleştirme** – Bu ek adım Microsoft tarafından gerekli değildir. Bu, müşterinin kararına ve müşterinin kendi zaman çizelgesine göre yapılır. Bu adım sırasında, müşteri verileri, Finance veya Project Operations ortamı gibi varolan bir ortama taşınmıştır. Bu, genellikle el ile ve Veri Yönetimi Çerçevesi (DMF) veri varlıkları kullanılarak yapılabilir. 

## <a name="planning-a-human-resources-environment-migration"></a>Human Resources ortam geçişi planlama

Altyapı birleştirmenin bir parçası olarak, tüm müşteriler varolan Human Resources ortamlarını bağımsız altyapıdan geçirmek zorundadır. Bu işleme yardımcı olması amacıyla, geçerli ortamlarınızı yeni altyapıya taşımak için, Lifecycle Services'ta otomatik geçiş aracı kullanmanızı öneririz. 

Aşağıdaki bölümlerde, tek başına Human Resources ortamı taşımak için Lifecycle Services araçlarının nasıl kullanılacağı hakkında daha fazla ayrıntı sağlanmaktadır. 

Bir geçiş planlaması yapan müşteriler aşağıdaki beklentileri içerebilir:

- Tüm müşteriler, üretim ortamını geçirmeden önce bir korumalı alan ortamına geçebilir. 
- Geçiş aracı yalnızca korumalı alandan korumalı alana ve üretimden üretime geçişini etkinleştirir. Bu nedenle, ortam türü hangi ortamın uygun şekilde geçirilebileceği belirleyecektir. 
- Müşteriler, hedef korumalı alan yuvası kullanılabilir durumda olacak şekilde, üretim ortamını geçirmeden önce gereken sayıda sanal alana geçiş yapabilirler. Müşteriler geçirilmiş bir korumalı alanı silebilir ve birden çok kere yeniden geçiş yapabilir. 
- Bir korumalı alan geçişi başarısız olduysa veya baştan başlamak istiyorsanız, finans ve operasyonlar altyapısında bir ortam silip aynı ortamı yeniden geçirebilirsiniz.
- Human Resources ortamınızın URL'si geçişten sonra farklı olacaktır.
- Üretim ortamınızın geçişi için uygun bir kesinti süresi planlayın. Otomatik geçiş işleminin tamamlanması için tahmini zaman dilimi üç ile dört saat arasında bir işlemdir. Zaman dilimi, kuruluşunuzun verilerine bağlı olarak değişir. Korumalı alan ortamlarınızın taşınması sırasında gerekli olan zaman miktarını doğrulamanız ve tamamlanması gereken ek el ile görevler için zaman vermeniz gerekir.

> [!IMPORTANT] 
> Üretim ortamı, finans ve operasyonlar alt yapısına başarılı bir şekilde geçirildiğinde, kaynak tek başına üretim ortamı otomatik olarak silinir. Geçirilen üretim ortamı silinmemelidir. 

Geçiş işlemi çoğunlukla otomatiktir. Ancak, iş kullanıcılarınızın geçişten sonra bazı adımları ve doğrulamaları el ile tamamlaması gerekir.

Aşağıdaki el ile yapılan adımların tamamlanması gerekiyor:

- Geçiş için yeni bir Lifecycle Services projesi oluşturun.
- Tüm tümleştirme konfigürasyonuna göre yeni URL/son noktalara tümleştirmeyi göstererek eski ortamınızdaki tüm bütünleşmeleri yeni ortama göre düzeltin.
- Katıştırılmış Power BI raporlar için veri deposunu yenile.
- DMF çalışma alanından veri varlığı listesini yenile.
- Yardım için Lifecycle Services bağlantısı.
- Mali takvimler oluştur.

Otomatik işlem sırasında aşağıdaki eylemler tamamlanmalı ve doğrulanmalıdır:

- Veriler:

    - Yapılandırmalar
    - Güvenlik rolleri (özel roller dahil)
    - İş akışları (bildirimler dahil)
    - Kişiselleştirilmeler ve kaydedilmiş görünümler
    - Hareketler
    - Özel alanlar
    - Ekler
    - Uyarılar

- Veri yönetimi – Kendi veritabanınızı getirme (BYOD).
- Özellik yönetimi – Etkin/devre dışı özellikler.
- Katıştırılmış Power Apps.
- Power Platform yönetim merkezi bağlı ortam (yalnızca üretim).
- Toplu İşler.
- Her tüzel kişilik için boş bir genel muhasebe oluşturulur. Her bir genel muhasebe için varsayılan döviz kuru türü ve muhasebe para birimi belirlenir.
- Yeni bir hesap planı otomatik olarak oluşturulur ve her tüzel kişilikte **Genel muhasebe** sayfasına bağlanır. Human Resources ortamınızda konfigüre edilen mali boyutları, otomatik olarak yeni bir hesap yapısına eklenir ve genel muhasebeye bağlanır. 

> [!NOTE]
> Finans ve operasyonlar altyapısında, Dynamics 365 Finance ürününün bir parçası olarak bir genel muhasebe gereklidir. Dynamics 365 Human Resources bağımsız uygulamasında varolan özel boyut denetleyicisi yoktur. Human Resources birleştirilmiş alt yapısı, **Human Resources** modülünde mali boyutları göstermek için finans mantığına bağlıdır. Hesap planı ve finansal boyutlar hakkında daha fazla bilgi edinmek için [buraya](../finance/general-ledger/plan-chart-of-accounts.md) bakın. 

## <a name="considerations"></a>Dikkat Edilmesi Gereken Konular

- Ortamlara geçiş her zaman genel olarak kullanılabilen (GA) en son sürümde olacaktır. Geçiş ve test planınıza bağlı olarak korumalı alan ortamları için geçiş doğrulamanız farklı bir sürümde ise korumalı alan geçişinizi, üretim ortamınızla aynı sürüm üzerinden doğrulamanızı öneririz. 
- Geçiş sırasında, geçirilen ortamlar kaynak tek başına Human Resources ortamları ile aynı bölgeye yerleştirilir.

## <a name="licensing"></a>Lisans

Dynamics 365 Human Resources için aşağıdaki alanlarda lisansla ilgili herhangi bir değişiklik yoktur: 

- **Minimum lisans satın alma gereksinimi**
- **Üretim ve korumalı alan ortamı lisansları** – Mevcut bir bağımsız Human Resources kaynağınız bir adet üretim ortamı ve bir adet korumalı alan ortamı sağlıyorsa finans ve operasyonlar altyapısında da ek bir ücret olmadan aynı sayıda lisansa sahip olursunuz.
- **Ek korumalı alan lisansları** – Bağımsız Human Resources uygulaması için ek korumalı alan lisansları satın aldıysanız standart kabul testi (korumalı alan) ortamı için finans ve operasyonlar altyapısında ek bir ücret olmadan aynı sayıda korumalı alan lisansları kullanılabilir. 

---
title: "Şirket içi ortamlar için donanım boyutlandırma gereksinimleri"
description: "Şirket içi ortamlar için donanım boyutlandırma gereksinimleri"
author: kfend
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: chwolf
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 4a1cab8c126ad063a52827421d2ea1104d0c7287
ms.contentlocale: tr-tr
ms.lasthandoff: 07/27/2017

---

# <a name="hardware-sizing-for-on-premises-environments"></a>Şirket içi ortamlar için donanım boyutlandırma
Şirket içi ortam için donanım ve altyapı boyutlandırmaya başlamadan önce, [Sistem gereksinimleri](../get-started/system-requirements.md) ve [Kurulum ve dağıtım yönergeleri](../deployment/setup-deploy-on-premises-environments.md) belgelerini okuyun ve altyapı hakkında derinlikli bilgi sahibi olun. 

  **Not:** Optimum performans için sistem en iyi uygulamalarına dikkat edin. 

Belgeyi gözden geçirdikten sonra, hareket ve eş zamanlı kullanıcı hacminizi tahmin edebilir ve ortalama çekirdek çıkışına dayanarak ortamınızı boyutlandırabilirsiniz.

## <a name="factors-that-affect-sizing"></a>Boyutlandırmayı etkileyen faktörler
Aşağıdaki görselde gösterilen tüm faktörler boyutlandırmaya katkıda bulunur. Daha ayrıntılı bilgi toplandıkça boyutlandırmayı daha hassas şekilde belirleyebilirsiniz. Destekleyici veri olmadan donanım boyutlandırmanın tutarlı olması olası değildir. Gerekli veri için minimum gereksinim saat başına hareket hat yükünün tepe noktasıdır. 

[![Şirket içi ortamlar için donanım boyutlandırma](./media/lbd-sizing-01.png)](./media/lbd-sizing-01.png)

Soldan sağa bakıldığında, boyutlandırmayı doğru şekilde tahmin etmek için ilk ve en önemli faktör bir hareket profili veya hareket nitelendirmedir. Saat başına tepe hareket hacmini her zaman bulmak önemlidir. Birden fazla tepe dönemi varsa, bu dönemlerin doğru olarak tanımlanması gerekir. 

Yüküm altyapınızı nasıl etkilediğini anladığınızda, bu faktörler hakkında daha fazla ayrıntıyı anlamanız gerekir: 

- **Hareketler** - Hareketlerin genellikle gün/hafta boyunca çeşitli tepe noktaları vardır. Bu genellikle hareket türüne bağlıdır. Zaman ve gider girişleri genellikle haftada bir tepe noktası gösterirlerken Satış siparişi girişleri gün içerisinde tümleştirme veya trickle yolu ile gelirler. 

- **Eş zamanlı kullanıcıların sayısı** – Eş zamanlı kullanıcıların sayısı ikinci en önemli boyutlandırma faktörüdür. Eş zamanlı kullanıcıların sayısına dayanarak güvenilir boyutlandırma elde edemezsiniz, bu yüzden de kullanabileceğiniz tek veri buysa, bir yaklaşık sayı tahmin edin ve bunu daha fazla veriniz olduğunda elden geçirin. Doğru bir eş zamanlı kullanıcı tanımı şu anlama gelir: 
  - Adlandırılmış kullanıcılar eşzamanlı kullanıcı değildir.
  - Eş zamanlı kullanıcılar adlandırılmış kullanıcıların her zaman bir alt kümesidir. 
  - Tepe iş yükleri boyutlandırma için maksimum eş zamanlılığı tanımlar.
 
- Eş zamanlı kullanıcılar için ölçüt, kullanıcının aşağıdaki ölçütlerin tümüne uymasıdır: 
  - Oturum açmış. 
  - Sayım sırasında çalışan hareketler/sorgular. 
  - Kullanılmayan bir oturum değil. 
 
- **Veri bileşimi** – Bu çoğunlukla sisteminizin nasıl ayarlanıp yapılandırılacağıyla ilgilidir. Örneğin, kaç adet tüzel kişiliğe, kaç tane maddeye, kaç tane ürün reçetesi düzeyine sahip olacaksınız ve güvenlik kurulumunuz ne kadar karmaşık olacak. Bu faktörlerin her biri performansınız üzerinde küçük bir etkiye sahip olacaktır, bu yüzden de bu faktörler, altyapı sözkonusu olduğunda akıllı tercihlerde bulunarak denkleştirilebilir. 

- **Uzantılar** – Özelleştirmeler basit veya karmaşık olabilir. Özelleştirmelerin sayısı ve karmaşıklığın doğası ve kullanımı, gerek duyulan altyapının boyutunu çeşitli şekillerde etkileyebilir. Örnek özelleştirmeler için, sadece verimliliği test etmekle kalmak için değil, aynı zamanda altyapı ihtiyaçlarını anlamaya yardımcı olmak için de performans değerlendirmeleri yapmak tavsiye edilir. Uzantılar performans ve ölçeklenebilirlik için en iyi yöntemlere uygun olarak kodlanmadıysa daha da önemlidir. 

- **Raporlama ve analizler** – Bu faktörler genellikle ağır sorgularını, Finance and Operations veritabanları sistemlerinde çeşitli veritabanlarına karşı çalıştırır. Pahalı raporların çalıştırılma sıklığını anlamak ve azaltmak, bunların etkisini daha iyi anlamanıza yardımcı olacaktır. 

- **Üçüncü taraf çözümler** – Bu çözümler, ISV'ler gibi, uzantılarla aynı çıkarımlara ve önerilere sahiptir. 

## <a name="sizing-your-finance-and-operations-environment"></a>Finance and Operations ortamınızı boyutlandırma
Boyutlandırma gereksinimlerinizi anlamak için işlemeniz gereken hareketlerin tepe hacmini bilmeniz gerekir. Yönetim Raporlayıcısı veya SSRS gibi çoğu yedek sistem, daha az kritiktir. Bunun sonucu olarak, bu belge çoğunlukla AOS ve SQL Server'a odaklanır. 

**Not:** Genel olarak, hesaplama katmanları ölçeklenir ve N+1 şeklinde ayarlanmalıdır, bu da üç AOS tahmin ediyorsanız, dördüncü bir AOS eklemeniz anlamına gelir. Veritabanı katmanı her zaman açık yüksek kullanılabilirlik kurulumunda ayarlanmalıdır. 


## <a name="sql-server-oltp"></a>SQL Server (OLTP)

### <a name="sizing"></a>Boyutlandırma

- DB sunucusunda çekirdek başına saat başına 3K - 15K hareket satırı.
- Tipik AOS'tan SQL'e çekirdek oranı birincil SQL Server için 3:1'dir. Ek çekirdekler, seçilen yüksek kullanılabilirlik yapılandırmasına dayalı olarak gereklidir. 
  - Veritabanının yoğun olarak işleyen işlemlerin işlenmesi bunu 2:1'e geriletebilir. 
- Aşağıdaki etkenler değişimleri etkiler: 
  - Kullanımda olan parametre ayarları. 
  - Eklenti düzeyleri. 
  - Veritabanı günlüğü ve uyarılar gibi ek işlevlerin kullanımı. Ekstrem veritabanı kaydı alma saat başına çekirdek başına çıkışı 3K satır altına çekecektir. 
  - Veri bileşiminin karmaşıklığı – Basit bir hesap planına karşılık ayrıntılı bir hesap planının çıkış üzerine etkileri vardır (örnek olarak). 
  - Hareket nitelendirme.
  - Her bir çekirdek için 2 GB - 4 GB arası bellek 
  - DB sunucusu üzerinde Yönetim raporlayıcısı ve SSRS veritabanları gibi yedek veritabanları.
  - Temp DB = veritabanı boyutunun %15'i, fiziksel işlemciler kadar fazla sayıda dosya ile. 
  - SAN boyutu ve çıkış, toplam eş zamanlı hareket hacmi/kullanımına dayalıdır. 

### <a name="high-availability"></a>Yüksek kullanılabilirlik 
SQL Server'ı her zaman bir küme veya yansıtma kurulumunda kullanmanızı öneririz. İkinci SQL düğümü, birincil düğüm ile aynı sayıda çekirdeğe sahip olmalıdır. 

### <a name="active-directory-federation-services-ad-fs"></a>Active Directory Federasyon Hizmetleri (AD FS)
AD FS boyutlandırma için bkz [AD FS Sunucu Kapasite belgeleri](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/design/planning-for-ad-fs-server-capacity).

Bir [boyutlandırma elektronik tablosu](http://adfsdocs.blob.core.windows.net/adfs/ADFSCapacity2016.xlsx) dağıtımınızdaki örneklerin sayısını planlamak için kullanılabilir.

<a name="aos-online-and-batch"></a>AOS (Çevrimiçi ve toplu iş)
----------------------

### <a name="sizing"></a>Boyutlandırma

- Hareket hacmi/kullanıma göre boyutlandırma
  - Çekirdek başına 2K - 6K satır
  - Örnek başına 16 GB
  - Standart kutu – 4 - 24 arası çekirdek
  - Çekirdek başına 10 - 15 Kurumsal kullanıcı
  - Çekirdek başına 15 - 25 Faaliyet kullanıcısı
  - Çekirdek başına 25 - 50 Takım üyesi
- Toplu İş
   - Çekirdek başına 1 - 4 toplu iş iş parçacığı
   - Toplu iş pencere nitelendirmesine göre boyut
- AOS, Veri Yönetimi ve Toplu işin Service Fabric'te aynı rolde olduğunu unutmayın. Bu üç iş yükünü birleştirerek boyutlandırmanız, bunları Microsoft Dynamics AX'teki gibi ayırmamanız gerekir.
- SQL Server için aynı değişkenlik faktörleri burada da geçerlidir.

### <a name="high-availability"></a>Yüksek kullanılabilirlik
- Tahmin ettiğinizden 1-2 adet daha fazla kullanılabilir AOS'e sahip olduğunuzdan emin olun.
- En az 3-4 sanal ana bilgisayara sahip olduğunuzdan emin olun.

## <a name="management-reporter"></a>Yönetim raporlayıcısı
Çoğu durumunda ve yaygın olarak kullanılmadığında, iki düğümün kullanılmasıyla önerilen minimum gereksinimler iyi iş görecektir. Yalnızca ağır kullanımınız söz konusu olduğu durumlarda ikiden fazla düğüme ihtiyaç duyarsınız. Lütfen gerektiği şekilde ölçeklendirin.

## <a name="sql-server-reporting-services"></a>SQL Server Reporting Services
Genel kullanım sürümü için yalnızca bir SSRS düğümü dağıtılabilir. SSRS düğümünüzü test ederken izleyin ve SSRS tarafından kullanılabilir çekirdeklerin sayısını ihtiyaca göre artırın. Önceden yapılandırılmış bir ikincil düğümün SSRS VM'den farklı bir sanal makinede kullanılabilir olduğundan emin olun. Bu, SSRS'yi barındıran sanal makine veya sanal ana bilgisayarda bir sorun olursa önemlidir. Bu durumda, bunların değiştirilmesi gerekir. 

## <a name="environment-orchestrator"></a>Ortam Orchestrator
Orchestrator hizmeti, dağıtım ve LCS ile ilgili iletişimi yöneten hizmetidir. Bu hizmet, birincil Service Fabric hizmeti olarak dağıtılır ve en az üç VM gerektirir. Bu hizmet Service Fabric düzenleme hizmeti ile birlikte yer alır. Bu, kümenin tepe yük noktasına göre boyutlandırılmalıdır. Daha fazla bilgi için bkz [Service Fabric küme kapasite planlama konusunda dikkate alınacaklar](/azure/service-fabric/service-fabric-cluster-capacity).  


## <a name="virtualization-and-oversubscription"></a>Sanallaştırma ve aşırı talep
AOS gibi pek çok kritik görev hizmetleri ayrılmış kaynaklara (çekirdekler, bellek ve disk) sahip Sanal ana bilgisayarlarda barındırılmalıdır.   


---
title: "Proje tahminleri ve bütçeler"
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 9577a7058986d200073d66a5824fbba29efa5125
ms.lasthandoff: 03/31/2017


---

# <a name="project-forecasts-and-budgets"></a>Proje tahminleri ve bütçeler

[!include[banner](../includes/banner.md)]




Microsoft Dynamics 365 for Operations projelerinizi yönetmeniz ve kontrol etmeniz için iki yöntem sunar: proje tahminleri ve proje bütçeleri. 

Organizasyonunuz bir operasyonel perspektife sahipse ve eğer belirli hareketlerden elde edilen gelirlere ve çıkan maliyetlere odaklanıyorsa tahmin yöntemini kullanın. Eğer organizasyonunuz daha çok mali tutarlara odaklanıyorsa proje bütçeleme yöntemini kullanın. 

Hem proje tahminleri hem de proje bütçeleri, öngörülen hareket tutarlarını tutmak için tahmin modelleri kullanır. 

Her yöntemin kendine göre avantajları vardır. Kuruluşunuz için bir yöntemi seçmeden önce aşağıdaki noktaları göz önünde bulundurmalısınız.

|                           |                                                                                                                                                                                                                                                         |                                                                                                                                                                         |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                           | **Proje tahmini **                                                                                                                                                                                                                                 | **Proje bütçelendirmesi **                                                                                                                                                   |
| **Dönem tahsisatı **     | Bir mali dönemdeki hareketlerini açıkça ayrılamıyorsunuz. Bunun yerine, tahmin ve tahmin denetimi, projenin yaşamını temel alır. Tahminler belirli bir tarih tabanlı olduğundan, dönemi tarihten anlamlandırmalısınız. | Hareketleri bir projenin tamamı ya da bir mali dönem üzerine tahsis edebilirsiniz. Bir döneme tahsis ederseniz, kullanılmayan tutarları sonraki mali döneme ileri taşıyabilirsiniz. |
| **Hareketleri görüntüleme**  | Hiyerarşi ne olursa olsun, hareketleri tahmin formlarında, tüm şirket ve tüm projeler için görüntüleyebilirsiniz. Belirli bir proje üzerinde odaklanmak için verilere filtre uygulamak gerekir.                                       | Tek bir proje hiyerarşisi için bütçe hareketlerini görüntüleyebilirsiniz. Bu nedenle, bir ana proje veya onun alt projeler için hareket ayrıntıları görüntüleyebilirsiniz.                 |
| **Hareket değişkenleri ** | Tahmin hareketleri girdiğinizde, gerçek bir hareket için var olan her özniteliği kullanabilirsiniz. Bu daha ayrıntılı olarak tahmin sağlar. Örneğin, miktarlar, çalışanlar, öğeler veya satır özellikleri için ayrıntıları girebilirsiniz.         | Bütçe ayrıntılarını girdiğinizde, yalnızca tutarlar, kategoriler ve faaliyetleri kullanabilirsiniz.                                                                                    |
| **Güvenlik **              | Taminler, tahmin formlarına girdiğiniz hareketlere dayanır ve hiçbir işlem denetim mekanizması içermez. Tahmin formu için izinleri olan herhangi bir çalışan onayı olmadan bilgileri gözden geçirebilir.                                        | Bütçeleme, iş akışı sistemini kullanır, bu da yönetimi değiştirmenizi ve revizyonların geçmişini tutmanıza olanak sağlar.                                                       |
| **Giriş türleri **           | Tahmin hareket girişleri, birimlerin sayısı ve satış birimi fiyatlarını ve maliyetleri temel alır.                                                                                                                                                       | Bütçe ayrıntıları, maliyetleri ve gelirler arasında bölünen tutarları temel alır.                                                                                        |
| **Tahmin modelleri**       | Her tahmin modeli bir model ile ilişkili olması gerektiğinden, birden fazla tahmin modeli oluşturabilir ve ayrıca alt modeller ayarlayabilirsiniz.                                                                                                                               | Proje Bütçeleme, bütçeleme için kullanılan tahmin modellerini sınırlar. Daha az tahmin modelleri, tahminlerin tutarlılığını artırmaya yardımcı olabilir.                           |
| **Maliyetini aşan öğeler **         | Yalnızca maliyet taşmasına neden olan hareketlerin girişine izin verebilir veya vermeyebilirsiniz.                                                                                                                                                                | Proje bütçeleme kullanıcılara ek denetim seçenekleri sağlar. Uyarılara ve taşmalara izin verebilirsiniz.                                                                   |
| **Denetim**               | Tahmin denetimi, tahmin azaltması kullanılarak gerçekleştirir. Fiili tutarlar, herhangi bir denetim izi olmadan tahmin hareketlerinin bakiyesinden çıkartılır. Bu,gerçek hareketlerin nerede meydana geldiğini izlemeyi güçleştirebilir.                   | Proje Bütçe denetimi içinde, gerçek tutarlar, kalan bütçedeki tutarlardan çıkartılır. Bu daha anlaşılır bir denetim izlemesini sağlar.                                   |

## <a name="project-forecasts"></a>Proje tahminleri
Proje tahmini kullandığınızda, her hareket tipi için tahmin formlarında tahmin hareketlerini girebilirsiniz. Gerçek bir hareket için kullanılabilir olan her öznitelik, bir tahmin hareketi için de kullanılabilir — örneğin satır karlılığı, satır öznitelikleri, çalışanlar veya açıklamalar. Ayrıca bir maliyete tabi olduktan ne kadar sonra bir müşteriye faturalandırılabileceğini tahmin edebilirsiniz. 

Proje tahmin hareketleri, birimleri ve tutarları temel alır. 

Her proje tahmininin bir tahmin modeli ile ilişkilendirmeniz gerekir. Bir tahmin hareketi girdiğinizde, bir tahmin modeli otomatik olarak önerilir. Tahmin modeli, tahmin hareketleri için bir kapsayıcı olarak davranır. 

Tahmin modellerini, bir model için alt model olarak belirleyebilirsiniz. Bu bölge, süre veya departman üzerinden tahmin oluşturmanızı sağlar. Bir modeldeki tahmin hareketlerini yeni bir model oluşturmak için kopyalayabilir ve ayrıca hareketleri genel muhasebeye aktarabilirsiniz. Tahmin ve model arasında bire bir ilişki olduğundan, her tahmin modeli ayrı proje için bir bütçe oluşturur. 

Tahmin modelleri projelerin denetim mekanizması olarak tahmin azaltmayı kullanabilirler. Tahmin azalmada, gerçek hareketler tahmin hareketlerinin bakiyesini azaltır. Ancak, tahmin azaltması proje hiyerarşisinde en yüksek öncelikle uygulandığından, tahmindeki değişimler hakkında sınırlı bir görünüm sağlar. Örneğin, bir çalışan bir alt proje ile ilişkilendirilmişse, çalışan için gerçek hareketler ana projeye nakledilir. Bu da değişimleri izlemeyi zor hale getirebilir çünkü hangi alt projedeki hangi hareketin, tahmin tutarında azaltmaya sebep olduğunu tespit etmeniz kolay olmaz. Bu nedenle, tahmin azaltmasının kullanması için tahmin modelinin bir kopyasını oluşturmak iyi bir fikirdir. Sonra raporları kullanıp başlangıçta tahminin ne olduğunu görüntüleyebilirsiniz. 

Proje tahminlerini genel muhasebe bütçesinde gözden geçirebilirsiniz, kopyalayabilir, silebilir veya transfer edebilirsiniz. Ancak, hiçbir işlem denetimi yoktur. Tahmin formu için izni olan herhangi bir çalışan gözden geçirme olmadan revizyon yapabilir.

-   **Gözden geçirme** – Özgün girişlerin yapıldığı formlarda tahmin hareketlerini düzeltebilirsiniz.
-   **Kopyala veya sil** – Tahmin hareketlerini kopyaladığınızda, hareket satırını bir tahmin modelinden bir diğer tahmin modeline kopyalarsınız. Bir tahmini sildiğinizde, bir tahmin modelinden tahmin hareketlerini silersiniz. Kopyalanan veya silinen tahmin hareketlerini sınırlandırmak için belirli hareket tipleri ve tarihleri seçin. Bu sadece bir tahminin belirli kısımlarını kopyalamanıza veya silmenize izin verir.
-   **Transfer** – Bir proje tahminini genel muhasebe bütçesine aktardığınızda, bir tahmin modelinin tahmin hareketlerini genel muhasebe defterine aktarırsınız. Proje tahmininizi transfer ettiğiniz genel muhasebe bütçe modeline önceden transfer edilen hareketleri değiştirebilirsiniz.

## <a name="project-budgets"></a>Proje bütçeleri
Proje bütçeleme, tahmine göre daha basit bir yöntem olmasına rağmen tahmin modelleriyle tümleştirme sağlar. Orijinal bütçe ayrıntıları ve düzeltmeler için tek bir giriş formu kullanır ve yalnızca tutar, kategori veya etkinlik tabanlı tahminlere izin verir. 

Proje Bütçeleme'de, tüm özgün bütçeler ve düzeltmeler onay için bir proje iş akışına gönderilmelidir. İş akışları size işlem üzerinde artırılmış denetim sağlar ve değişiklik geçmişi kaydı oluşturur. 

Proje Bütçeleme genel muhasebe bütçelemesine benzer, ancak ayarlanması daha hızlı ve kolaydır. Genel muhasebe bütçelemesindeki seçeneklerin çoğunun, örneğin numara serileri veya para birimi gibi, projeler için ayrıca ayarlanmasına gerek yoktur.

Proje bütçeleri otomatik olarak iki tahmin modeliyle ilişkilendirilir, biri orijinal bütçe için, diğerikalan bütçe için. Bu nedenle, tahmin modellerine dayanan raporlar bütçe verilerini kullanabilirler. Bir proje bütçesi işlendiğinde, sistem tahmin hareketlerini, raporlama ve denetim amaçları için kullanılan, ilişkilendirilen modellere dayanarak oluşturur.

## <a name="forecast-models"></a>Tahmin modelleri
Tahmin modellerinin tek katmanlı bir hiyerarşisi vardır. Bu da başka bir deyişle bir proje tahmininin, bir tahmin modeliyle ilişkilendirilmesi gerektiği anlamına gelir.

Proje tahmini kullanırsanız, modelleri alt model olarak tanımlayabilirsiniz. Tahminleri departmana, süreye veya bölgeye göre oluşturabilirsiniz. Örneğin, bir yıl için bir tahmin modeli oluşturabilir ve sonra Kuzeydoğu, Güneydoğu, Kuzeybatı ve Güneybatı için bölgesel tahminleri için bölge başkanlarının göndereceği alt modeller oluşturabilirsiniz. Kullanılabilir raporlarda farklı seçenekleri belirleyerek, toplam tahmine veya alt modele göre bilgileri görüntüleyebilirsiniz.





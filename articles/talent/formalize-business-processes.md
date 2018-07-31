---
title: "İş süreçlerini biçimlendirme"
description: "Bu konuda, kuruluşunuzda tamamlanması gereken süreçlere ilişkin bir iş süreci şablonu oluşturmak için İş süreci özelliğini nasıl kullanabileceğiniz açıklanmaktadır."
author: ShielaSogge
manager: AnnBe
ms.date: 01/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: PersonnelBusinessProcessGenericWorkspace, BusinessProcessGenericTemplateListpage, BusinessProcessGenericMyTemplates, BusinessProcessGroupAssignment
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: ShielaS
ms.search.validFrom: 2018-01-09
ms.dyn365.ops.version: AX 7.1.0, Talent October 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ee4035f3156a91faecdecba45289dbb1ca6e947a
ms.openlocfilehash: fd538677d897c1e7d3103cd714c688373aab8d29
ms.contentlocale: tr-tr
ms.lasthandoff: 06/19/2018

---
# <a name="formalize-business-processes"></a>İş süreçlerini biçimlendirme

[!include[banner](includes/banner.md)]

İş süreci özelliği, kuruluşunuzda tamamlanması gereken iş süreçleri için bir iş süreci şablonu oluşturmanıza olanak sağlar. Örneğin şirketiniz her yıl bir İnsan Kaynakları (HR) denetimi tamamlıyor. Bu durumda, denetim sürecini oluşturan tüm görevlerin izlendiği bir şablon oluşturabilirsiniz. Bu şablon, her denetim yapıldığında tüm görevlerin yerine getirilmesinin garanti edilmesine yardımcı olabilir. Ayrıca, görevlerin belirli bir sırayla tamamlanması gerekiyorsa, şablon bu görevlerin doğru sırada yapılmasını garantilemeye de yardımcı olabilir.

Şablonlar, yinelenen süreçler için yeniden kullanılabilir. Bunlar aynı zamanda kopyalanabilir ve yeni şablonlar oluşturmak için başlangıç noktası olarak kullanılabilir.

Bir iş süreci şablonu oluşturulduktan sonra, **İş süreci** çalışma alanında bir iş süreci başlatılıp izlenebilir. Bir iş süreci başladığında, görevler ilgili kişilere atanır ve birer son tarih içerir.

## <a name="business-process-templates"></a>İş süreci şablonları
Bir iş süreci şablonu, iş sürecini oluşturan görevler grubunu listeler. İnsan kaynakları yöneticileri ve yardımcıları varsayılan olarak iş süreçleri oluşturabilir. Bununla birlikte, iş süreçlerini oluşturabilecek rolleri, güvenlik yapılandırmasındaki **Genel iş süreçlerini koru** görevinde değişiklik yaparak değiştirebilirsiniz.

Her bir iş süreci için bir süreç sahibi tanımlayabilirsiniz. Süreç sahibi süreçteki tüm görevleri görebilir ve görevleri yeniden atayabilir veya son tarihleri değiştirebilir. Örneğin İnsan Kaynakları direktörü, kazançları incelemek için bir iş süreci şablonu oluşturur ve süreç sahibi olarak Ücret ve kazançlar yöneticisini belirtir. Bu durumda Ücret ve kazançlar yöneticisi, inceleme sürecinin bir parçası olarak, tamamlanması gereken görevleri görme yetkisi kazanır.

Süreç sahibi yeni iş süreçleri veya iş süreci şablonları oluşturamaz, etkin iş süreçlerini veya iş süreci şablonlarını silemez.

## <a name="tasks"></a>Görevler
İş süreci genellikle birden çok görevden oluşur. Dahili kurs tekliflerinin incelenmesi gibi bazı görevler Microsoft Dynamics 365 for Talent'ta[?] tamamlanabilir. Bu durumda **Görev bağlantısı** alanında bir seçenek belirlenir. Bir web sitesindeki sayfaların incelenmesi veya tamamlanması gibi başka görevler de olabilir. Bu durumda, **Görev bağlantısı** alanında **URL** seçilip ardından web adresi girilebilir. Hem dahili hem de harici sitelerin URL'lerini girebilirsiniz. Ayrıca, tüm yapılara erişilebilirliği inceleme gibi el ile tamamlayabileceğiniz faaliyetlerle ilgili görevler de oluşturabilirsiniz. Bu durumda görev bağlantısı gerekli değildir. Bu esneklik, çeşitli türlerdeki görevleri kapsamlı bir süreçte izlemenize olanak tanır.

Görevler belirli bir çalışana veya bir pozisyona atanabilir. Örneğin, Ücret ve kazançlar yöneticisi her zaman sigorta primleri incelemesi yapan kişi olacaktır. Bu nedenle, bu görevi oluştururken, **Atama türü** alanında **Pozisyon**'u ve ardından **Pozisyon** listesinden **Ücret ve kazançlar yöneticisi**'ni seçin. İş süreci başlatılınca, görev **Ücret ve kazançlar yöneticisi** pozisyonunda bulunan çalışana atanır. Bir görevi belirli bir çalışana atamak için, **Atama türü** alanında **Çalışan**'ı ve ardından ilgili kişiyi seçin.

Görevlerin son tarihleri, iş süreci başlatılırken girilen hedef tarihine bağlıdır. Bazı görevlerin hedef tarihinden önce tamamlanması gerekirken, diğer görevler hedef tarihinden sonra tamamlanabilir. Bir görevi tanımlarken, **Hedef tarihinden itibaren vade tarihi mahsuplaştırma** alanında hedef tarihine göre bir son tarih belirtirsiniz. Örneğin, Ücret ve kazançlar yöneticisinin, İK denetimi tamamlanmadan 10 gün önce sigorta primleri incelemesini yapması gerekiyor. Bu durumda, inceleme için oluşturulan görevin **Hedef tarihinden itibaren vade tarihi mahsuplaştırma** değeri **-10** olur. Bu nedenle, iş süreci 13 Mayıs'ta başlıyorsa, görevin son tarihi 3 Mayıs olacaktır.

> [!NOTE]
> Son tarihler iş süreci başlatıldıktan sonra da ayarlanabilir.

Karmaşık görevler için birden fazla adım gerekebilir veya görevleri uygulayan kişilerin ek bilgiler vermesi gerekebilir. Bu senaryolar için bir göreve yönergeler ekleyebilirsiniz. Yönergeler, görevin atandığı kişiye görevin nasıl tamamlanacağı konusunda ek bilgiler verebilir. Yönergelere zengin metin biçimlendirmesi dahi ekleyebilirsiniz.

## <a name="starting-a-business-process"></a>İş sürecini başlatma
Bir iş süreci şablonunda, iş sürecini **İşlemi başlat**'ı seçerek başlatabilirsiniz. Bir süreç başlatıldığında, şablona eklenen görevlerde tanımlanan seçili çalışanlar ve/veya pozisyonlar için görevler oluşturulur. "Görevler" bölümünde açıklandığı gibi, hedef tarihten mahsup edilecek günler eklenerek veya çıkarılarak her görev için birer son tarih de atanır. Etkin iş süreçlerini **İş süreçleri** çalışma alanında görüntüleyebilirsiniz.

## <a name="employee-self-service"></a>Çalışan self servisi
Görev bir çalışana atandıktan sonra çalışan o görevi ve diğer atanmış görevlerinin tümünü **Çalışan self servisi** sayfasında görüntüleyebilir. Çalışan, kendisine atanmış her bir iş süreci görevinin adını ve açıklamasını, görevi tamamlamaya ilişkin yönergeleri ve ilgili kişinin adını görebilir. Çalışan, Microsoft Dynamics 365'teki ilgili sayfayı veya ilgili web sayfasını **Çalışan self servisi** sayfasından da açıp görevleri Devam ediyor, İptal edildi veya Tamamlandı olarak işaretleyebilir.

## <a name="business-process-workspace"></a>İş süreci çalışma alanı
İK uzmanları etkin iş süreçlerini **İş süreci** çalışma alanında görüntüleyebilir. Bu çalışma alanı tüm etkin süreçleri ve her biriyle ilişkili olan görevleri listeler. Kapsamlı görev listesi bitiş tarihine göre filtrelenebilir. Çalışma alanı, geciken görevleri ve İK uzmanına özel olarak atanmış olan görevleri de listeler. İK uzmanları tüm görevlerin durumunu güncelleştirebilir ve gerektiğinde iş sürecinin ilerlemesini sağlamak için görevleri yeniden atayabilirler.

## <a name="my-business-processes-workspace"></a>İş süreçlerim çalışma alanı
Süreç sahipleri kendilerine atanan etkin iş süreçlerini **İş süreçlerim** çalışma alanında görüntüleyebilirler. Bu çalışma alanı, kullanıcının sahip olduğu tüm etkin süreçleri ve ilişkili görevleri listeler. Kapsamlı görev listesi bitiş tarihine göre filtrelenebilir. Çalışma alanı, özel olarak süreç sahibine atanmış görevleri de listeler. Ayrıca, süreç sahibi tüm görevlerin durumunu güncelleştirebilir ve herhangi bir görevi yeniden atayabilir.

## <a name="navigating-business-processes"></a>İş süreçlerinde gezinme
Bir iş süreci şablonu oluşturmak veya kopyalamak ya da iş süreci başlatmak için İş süreçleri - Bağlantılar – İş süreçleri yönetimi'ne gidin. Bunun ardından aşağıdaki eylemleri gerçekleştirebilirsiniz:

- Yeni bir iş süreci şablonu oluşturmak için **Yeni**'yi seçin.
- Seçilen bir şablonu yeni şablona kopyalamak için **Şablondan kopyala**'yı seçin.
- Seçilen iş sürecini başlatmak, görevler atamak ve son tarihleri hesaplamak için **İşlemi başlat**'ı seçin.

Etkin süreçleri ve ilişkili görevleri görüntülemek için **İş süreçleri** çalışma alanını açın.



---
title: "İş süreçlerini biçimlendirme"
description: "İş süreci özelliği, kuruluşunuz içinde tamamlanması gereken işlemler için iş süreci şablonu oluşturmanıza olanak sağlar."
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 1b50a97f5e2fc94255ff71702faf91ab36e68eb4
ms.contentlocale: tr-tr
ms.lasthandoff: 04/13/2018

---
# <a name="formalize-business-processes"></a>İş süreçlerini biçimlendirme
İş süreci özelliği, kuruluşunuz içinde tamamlanması gereken işlemler için iş süreci şablonu oluşturmanıza olanak sağlar. Örneğin, şirketiniz her yıl bir İK denetimi yapıyor olabilir. Denetimin kapsadığı tüm görevleri izleyerek süreç her tamamlandığında tüm görevlerin gerçekleştirilmiş olmasını sağlamaya yardımcı olmak ve gerekirse görevlerin doğru sırayla yerine getirilmesine yardımcı olmak amacıyla bir şablon oluşturulabilir. Şablonları yinelenen süreçler için tekrar kullanılabilir veya yenilerini oluşturmak için başlangıç noktası olarak kullanmak üzere kopyalanabilir.

Bir şablon oluşturulduktan sonra, İş süreçleri çalışma alanından bir süreç başlatılıp izlenebilir.  İş süreci başladığında, görevler ilgili kişilere atanır ve son tarihi içerir. Aşağıda bu bileşenleri ayrıntılı biçimde ele alacağız.

## <a name="business-process-template"></a>İş süreci şablonu
Bir iş süreci şablonu, iş sürecini oluşturan görevler grubunu listeler. İnsan kaynakları yöneticileri ve yardımcıları varsayılan olarak iş süreçleri oluşturabilir.  Ancak bu, Genel iş süreçleri koru görevi düzenlenerek güvenlik yapılandırmasında değiştirilebilir.

Her süreç için bir Süreç sahibi tanımlanabilir. Süreç sahibi süreçteki tüm görevleri görebilir ve görevleri yeniden atayabilir veya sona erme tarihlerini değiştirebilir.  Örneğin, İK müdürü kazançları gözden geçirme için bir İş süreci şablonu oluşturabilir.  Maaş ve kazançlar yöneticisi Süreç sahibi olarak ayarlanabilir; böylece bu kişinin gözden geçirmenin bir parçası olarak tamamlanması gereken görevlerde öngörüleri olabilir.  Süreç sahibi etkin İş süreçlerini veya İş süreci şablonlarını oluşturamaz veya silemez.

## <a name="task"></a>Görev
İş süreci genellikle birden çok görevden oluşur. Dahili kurs tekliflerini gözden geçirme gibi bazı görevler Dynamics 365 for Talent içinden tamamlanabilir. Böyle bir durumda, Görev bağlantısı alanında bir Menü öğesi seçilir. Diğer görevler, formların bir web sitesi üzerinden incelenmesini veya doldurulmasını gerektirebilir. Görev bağlantısı alanındaki URL seçildiğinde girilecek web adresi etkinleşir. Bu alana hem dahili hem de harici sitelerin URL'lerini girebilirsiniz. Ayrıca, tüm yapılara erişilebilirliği gözden geçirme gibi el ile tamamlayabileceğiniz faaliyetlerle ilgili görevler de oluşturabilirsiniz. Bu durumda görev bağlantısı gerekli değildir. Bu esneklik, çeşitli türlerdeki görevleri kapsamlı bir süreçte izlemenize olanak tanır.

Görevler belirli bir çalışana veya pozisyona atanabilir. Örneğin, Maaş ve kazançlar yöneticisi her zaman sigorta primleri incelenmesi yapan kişi olacaktır.   Bu görevi oluştururken, Atama türü için Pozisyonu seçin ve ardından Pozisyon listesinden Maaş ve kazanç yöneticisini seçin. Süreç başlatıldığında, görev Maaş ve kazançlar yöneticisi pozisyonunda bulunan çalışana atanır. Ayrıca, Atama türü alanında Çalışan öğesini belirleyip uygun kişiyi seçerek görevi belirli bir çalışana da atayabilirsiniz.

Görev son tarihleri süreç başlangıcında girilen Hedef tarihe bağlıdır. Bazı görevlerin hedef tarihten önce tamamlanması gerekir, bazı görevler hedef tarihten sonra tamamlanabilir.  Bir görevi tanımlarken, Hedef tarihinden itibaren vade tarihi mahsuplaştırma alanına hedef tarihe göre bir sona erme tarihi girersiniz. Örneğin, Maaş ve kazançlar yöneticisinin İK denetimi tamamlanmadan 10 gün önce sigorta primleri incelemesi gerçekleştirmesi gerektiğini varsayalım. Oluşturulan görevin son hedef tarihe oranla -10 olacaktır. Bu nedenle, süreç 13 Mayısta başlarsa, görevin son tarihi 3 Mayıs olacaktır. Not: Son tarihler süreç başlatıldıktan sonra da ayarlanabilir.

Karmaşık görevler birden fazla adım gerektirebilir veya bu görevler için ek bilgiler sağlamak üzere görevlerin tek tek gerçekleştirilmesini gerekebilir. Göreve yönergeler ekleyebilir ve yönergeler için zengin metin biçimini kullanabilirsiniz. Yönergeler, görevin atandığı kişiye görevin nasıl tamamlanacağı konusunda ek bilgiler sağlayabilir.

## <a name="starting-a-process"></a>Bir süreci başlatma
Süreç İş süreci şablonunda Süreci başlat seçilerek başlatılabilir.  Bir süreç başlatıldığında, seçilen çalışanlar ve/veya İş süreci şablonuna dahil edilen görevlerde tanımlanan pozisyonlar için görevler oluşturulur. Hedef tarihten mahsup edilecek günler eklenerek veya çıkarılarak her görev için bir son tarih atanır (görev bölümündeki mahsup edilen günlerle ilgili bilgiye bakın). Etkin İŞ süreçleri İş süreçleri çalışma alanından görüntülenebilir. 

## <a name="employee-self-service"></a>Çalışan self servisi
Görev bir çalışana atandığında, çalışanlar atanan görevleri Personel self servisi sayfasından görebilir. Kendisine iş süreci görevi atanan personel Personel self servisi sayfasından görevi, görev açıklamasını, yönergeleri ve ilgili kişinin adını görebilir ve ilgili Dynamics365 sayfasını veya web sayfasını açabilir. Görevler devam ediyor, iptal edildi veya tamamlandı olarak işaretlenebilir.

## <a name="business-process-workspace"></a>İş Süreci Çalışma Alanı
İK uzmanları etkin iş süreçlerini İş süreci çalışma alanından görebilir. Çalışma alanı tüm etkin süreçleri ve her biri ile ilişkili olan görevleri listeler. Kapsamlı görev listesi bitiş tarihine göre filtrelenebilir. Sayfa ayrıca geciken görevleri ve özellikle İK uzmanına atanmış olan görevleri de listeler. Gerekirse tüm görevlerin durumunu güncelleştirebilir ve gerektiğinde iş sürecinin ilerlemesini sağlamak için görevleri yeniden atayabilirler.

## <a name="my-business-processes-workspace"></a>İş Sürecim Çalışma Alanı
Süreç sahipleri kendilerine atanan etkin iş süreçlerini İş Sürecim çalışma alanından görebilirler. Çalışma alanı tüm etkin süreçleri ve kullanıcının sahibi olduğu ilişkili görevleri listeler.  Kapsamlı görev listesi bitiş tarihine göre filtrelenebilir. Sayfa ayrıca özellikle süreç sahibine atanmış olan görevleri de listeler. Süreç sahibi tüm görevlerin durumunu güncelleştirebilir ve görevleri yeniden atayabilir.

## <a name="navigating-business-processes"></a>İş Sürecinde Gezinme
1. Bir İş süreci şablonu eklemek için İş süreçleri - bağlantılar - İş süreçleri yönetimi'ne gidin.
   - a.   Yeni, yeni bir şablon oluşturur.
   - b.   Şablondan kopyala, seçilen şablonu yeni bir şablona kopyalar.
   - c.   Süreci başlat, seçilen iş sürecini başlatır, görevleri atar ve bitiş tarihlerini hesaplar.  
2. Etkin süreçleri ve ilişkili görevleri görmek için İş süreçleri çalışma alanına gidin.


---
title: "Yardım genel bakış"
description: "Bu makale, Microsoft Dynamics 365 for Operations Yardım sistemi bileşenlerine genel bir bakış sunar. Makalede, kuruluşunuz için özel belgeleri ve eğitimi nasıl sağlayabileceğiniz açıklanmaktadır."
author: margoc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16381
ms.assetid: 018c148c-9cbd-41e0-8186-d75dbf66288f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 240060606c8a2955c3f0a0d47fb25b0cde64c187
ms.lasthandoff: 03/31/2017


---

# <a name="help-overview"></a>Yardım genel bakış

Bu makale, Microsoft Dynamics 365 for Operations Yardım sistemi bileşenlerine genel bir bakış sunar. Makalede, kuruluşunuz için özel belgeleri ve eğitimi nasıl sağlayabileceğiniz açıklanmaktadır. 

Dynamics 365 for Operations, iki ana bileşeni temel alan bir Yardım sistemi içerir:

-   Belgeleri sitesi
-   Görev kılavuzları

Makaleler hem de görev kılavuzları Dynamics 365 işlemleri için Yardım bölmesinde aşağıdaki ekran görüntüsünde gösterildiği gibi erişebilirsiniz. [![Yardım Bölmesi](./media/help-pane-ops-task-guides-1024x741.png)](./media/help-pane-ops-task-guides.png) bu makalede Yardım sistemi ve kuruluşunuz için nasıl özel belgeleri ve eğitim kaynakları oluşturabileceğiniz açıklanmaktadır.

## <a name="help-on-docsmicrosoftcom"></a>docs.microsoft.com hakkında Yardım
docs.microsoft.com sitesi ([docs.microsoft.com/dynamics365/operations](https://docs.microsoft.com/en-us/dynamics365/#pivot=solutions&panel=solutions_operations) Dynamics 365 işlemleri için ürün belgelerine birincil kaynağıdır. Site aşağıdaki özellikleri sunar:

-   **En güncel içeriğe erişim** – site bize bir daha hızlı verir ve oluşturmak için daha esnek bir şekilde sunmak ve ürün belgeleri güncelleştirmek. Bu nedenle, en son teknik bilgilerin erişimine sahip olmanızı garanti etmeye yardımcı olur.
-    **Uzmanlar tarafından yazılan içeriği** – site topluluk üyeleri hem içindeki hem de dışındaki Microsoft tarafından geliştirilmiş ürün belgelerine, daha zengin bir kümesi sağlar.
-   ** Farklı türde içerik ** – site erişimi hızla Dynamics 365 işlemleri için ilgili içerik Microsoft Office karışımı sunuları, görev kılavuzlar, videolar ve wiki makaleleri gibi farklı türde erişim sağlar.
-    **İş süreçlerini destekleyen içeriği** – iş süreci Modeler (BPM) Microsoft Dynamics ömrü Hizmetleri (LCS) yararlanır iş süreci – odaklanmış içerik site içerir.

Biz tüm içeriği bizim önceki Yardım wiki belgeler için geçirilen. Bizim yeni site ve çok olacak umuduyla hakkında çok mutluyuz.

### <a name="when-can-we-use-it"></a>Onu ne zaman kullanabiliriz?

Şu anda içerik üzerinde belgeleri okuyabilir--tam olarak ortak ve aranabilir oturum açması gerekmeden. İçeriği bulmak için sık kullandığınız arama motorlarından istediğinizi kullanabilirsiniz. GitHub hesabı ile oturum açarak seçerseniz, sitesinde makaleleri üzerinde yorum yapabileceği.


## <a name="task-guides"></a>Görev kılavuzları
Görev Kılavuzu adımları bir görev veya iş süreci boyunca size yol gösterir kontrollü, Destekli, etkileşimli bir deneyimdir. Yardım Bölmesi'nden (yürütme) görev Kılavuzu açabilirsiniz. Görev Kılavuzu ilk tıklattığınızda Yardım Bölmesi görev için adım adım yönergeleri gösterir. Yerelleştirilmiş görev kılavuzları kullanıma hazırdır. [![Okuma görünümünde görev Kılavuzu](./media/task-guide-ops-1024x742.png)](./media/task-guide-ops.png) destekli, etkileşimli bir deneyim başlamak için tıklatın **başlangıç görev Kılavuzu** Yardım bölmesinin altındaki. Siyah bir işaretçi açılır ve gerçekleştirmeniz gereken eylemi gösterir. Kullanıcı arabiriminde görünen yönergeleri izleyin ve verileri yönlendirildiği şekilde girin. [![Görev Kılavuzu adım yönerge](./media/task-guide-step-1-ops.png)](./media/task-guide-step-1-ops.png)**önemli:** görev Kılavuzu yürüttüğünüzde, girdiğiniz verileri gerçek. Bir üretim ortamındaysanız, veriler kullanmakta olduğunuz şirkette girilir.

### <a name="it-all-begins-with-task-recorder"></a>Tüm bu Görev Kaydedicisi ile başlar

Görev kılavuzları Görev Kaydedici kullanarak oluşturulur. Görev Kaydedici'yi kullanırken, Dynamics 365 for Operations Kullanıcı Arabiriminde yaptığınız tüm eylemler (menülere tıklamak, ayarları değiştirmek ve veri girmek gibi) kaydedilir. Kaydettiğiniz tüm adımlar toplu olarak görev kaydı olarak adlandırılır. Bir önceki bölümde açıklandığı gibi görev kayıtları Yardım bölmesinde görüntülenebilir ve görev kılavuzları olarak oynatılır. Ancak, görev kayıtlarını kullanmanın farklı yolları vardır:

-   **Görev kayıtlarını BPM'ye kaydetme** – Bir görev kaydını LCS'deki BPM kitaplığında bir hiyerarşi sırasına kaydedebilirsiniz. BPM'ye bir görev kaydını kaydettiğinizde, akış diyagramı oluşturulur ve kayıt adımları ile birlikte görüntülenir. **Not:** Dynamics 365 for Operations Yardım bölmesinde bir görev kaydetmeyi görüntülemek ve görev kılavuz olarak yürütmek için kaydı bir BPM kitaplığına kaydetmeniz gerekir.
-   **Görev kayıtlarını Word belgesi olarak kaydet** – Görev kaydını bir Microsoft Word belgesi olarak kaydederek, kuruluşunuz için yazdırılabilir eğitim kılavuzlarını kolaylıkla üretebilirsiniz.

Görev Kaydedicisi hakkında daha fazla bilgi için bkz: [Dynamics 365 görev Kaydedicisi işlemleri için](../user-interface/task-recorder.md).

### <a name="creating-customized-task-recordings"></a>Özelleştirilmiş görev kayıtları oluşturma

Kendi görev kayıtlarınızı oluşturabilirsiniz veya Microsoft'un sağladığı görev kaydını indirebilir ve özelleştirebilirsiniz. Bu nedenle, belirli Dynamics 365 for Operations uygulamanızı yansıtan, kuruluşunuz için özelleştirilmiş Yardım oluşturabilirsiniz. Dynamics 365 bölmesi işlemler yardımcı olmak için kaydı bir görevi görüntülemek ve görev kılavuz olarak oynamak için kayıt LCS BPM kitaplığa kaydetmek zorunda kalırsınız. Bir ortak iseniz ve bir şirket kitaplığına kitaplığa yükseltilir ve bir çözüme eklemek müşterileriniz için kullanılabilir olacaktır. Tam yönergeler için bkz: [belgelerine veya eğitim oluşturmak için görev kayıtlarını kullanarak](../user-interface/task-recorder.md).

## <a name="in-product-help"></a>Ürün içi Yardım
İşlemleri için Dynamics 365 içinde Yardım içeriğini erişmek için'ı tıklatın ya da **yardımcı** (**?**) simgesini ve sonra Yardım'ı seçin veya Ctrl + ÜstKrkt +?. Her iki durumda Yardım bölmesi açılır. Yardım Bölmesi'nden makaleler veya görev kılavuzları erişebilir. [![](./media/help-pane-wiki-1024x684.png)](./media/help-pane-wiki.png)

### <a name="accessing-articles-from-the-help-pane"></a>Yardım Bölmesi'nden makaleleri erişme

Yardım Bölmesi'nden Dynamics 365 işlemleri istemci için uygulanan makaleleri erişebilirsiniz. Ne zaman, ilk Yardım bölmesini açın ve'ı **Wiki** sekmesi, üzerinde içinde Dynamics 365 işlemleri için bulunduğunuz Sayfaya Uygula makaleleri göreceksiniz. Hiçbir makaleleri bulunursa, aramanızı daraltmak için anahtar sözcükler girebilirsiniz. Yardım Bölmesi'nde bir makale'ı tıklattığınızda, yeni bir sekme tarayıcınızda açılır ve makale görüntüler. 

### <a name="accessing-task-guides-from-the-help-pane"></a>Yardım Bölmesi'nden görev kılavuzları erişme

Yardım Bölmesi'nden görev kılavuzları erişmeden önce gitmek bir sistem yöneticisi olan **sistem parametreleri** Dynamics 365 işlemleri için sayfa ve bazı ayarları yapılandırın. **Notlar:**

-   Yardımı yapılandırmak için Dynamics 365 for Operations'ın dağıtıldığı kiracı ile aynı kiracı içindeki bir hesap ile oturum açmanız gerekir.
-   LCS kitaplığına, yerel bir sanal sabit sürücüde (VHD) çalıştırılan bir Dynamics 365 for Operations örneğinden bağlanmak mümkün değildir.

[![Sistem parametreleri formundaki Yardım ayarları ile](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) üzerinde **sistem parametreleri** sayfasında, aşağıdaki adımları izleyin:

1.  **Önemli: **Yardım sekmesini ilk kez açtığınızda Lifecycle Services'e bağlanmanız gerekir. Formun ortasýndaki bağlantıyı tıklatın, bağlantı için bekleyin, iletişim kutusunu kapatmak ve parametreleri forma almak için Tamam'ı tıklatın emin olun. [![LCS için bağlanma](./media/connect-to-lcs-crop-1024x365.png)](./media/connect-to-lcs-crop.png)
2.  Bağlanmak için Lifecycle Hizmetleri projesini seçin.
3.  Görev kayıtlarını almak için BPM kitaplıkları (Seçili proje içinde) seçin.
4.  BPM kitaplıklarının görüntülenme sırasını ayarlayın. Bu Yardım bölmesinde kitaplıklardaki görev kayıtlarının hangi sırayla görüneceğini belirler.

Bir sistem yöneticisi bu adımları tamamladıktan sonra Yardım bölmesini açıp **Görev kılavuzları** sekmesine tıklayabilirsiniz. Artık temel işlemleri için Dynamics 365 içinde bulunduğunuz Sayfaya Uygula görev kılavuzları görürsünüz. Hiçbir görev kılavuzları bulunursa, aramanızı daraltmak için anahtar sözcükler girebilirsiniz. Yardım Bölmesi'nde bir görev Kılavuzu'nu tıklatın, sonra yönergeleri adım adım Yardım Bölmesi gösterir ve görev Kılavuzu oynayabilirler. [![Okuma görünümünde görev Kılavuzu](./media/task-guide-ops-1024x742.png)](./media/task-guide-ops.png)

### <a name="where-are-the-translated-task-guides"></a>Çevrilmiş görev kılavuzları nerede?

"Tüm dillerde" başlığı ile yayımlanan kılavuzları kitaplıklarında görev çevrilir. Dynamics 365 işlemleri için yerelleştirilmiş görev Kılavuzu yardımcı olmak için bir apppropriate Kitaplığı'na bağlı olduğunuzdan emin olun. Görev kılavuz görünür dil, her kullanıcı için dil ayarları tarafından denetlenir **seçenekleri**&gt;**Tercihler**. 
-   Görev Kılavuzu görev Kılavuzu'nun tüm metin görünür, seçilen dilde açtığınızda, görev Kılavuzu çevrildikten varsa.
-   Açtığınızda bir görev kılavuz henüz, çevrildikten değil, yalnızca bazı metinler (denetimler metin), seçilen dilde görüntülenir.

## <a name="additional-resources"></a>Ek kaynaklar
Aşağıdaki tablo, Dynamics 365 for Operations içeriği sağlayan web sitelerini listeler. İçerik web sitelerimiz müşteri ömrünü desteklemek için düzenlenmiştir. Her aşama farklı bir site kümesi tarafından desteklenir. Yıldız işareti olmayan siteleri (\*) adının yanında, bir hizmet planı ile ilişkili olan bir hesabı kullanarak oturum açabilmenizi sağlar.

| Tesis                                                                     | Açıklama                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Docs.microsoft.com](https://docs.microsoft.com/en-us/dynamics365/#pivot=solutions&panel=solutions_operations) | Dynamics 365 for Operations için tüm ürün belgelerini barındırır veya bunlara bağlantı kurar.                                                                                                                                                               |
| [Lifecycle Services](http://lcs.dynamics.com/en/)\*                      | Müşteriler ve ortakların satış öncesinden uygulama ve işlemlere kadar Dynamics 365 for Operations projelerini yönetebilmesi için bulut-tabanlı iş birliğine dayalı çalışma alanı sağlar. Bu site uygulamanın tüm aşamalarında yararlıdır. |
| [CustomerSource](http://www.customersource.com/)\*                       | Kapsamlı eğitim kaynaklarını barındırır ve Dynamics 365 for Operations için birincil destek sitesidir. Sitedeki belirli kaynaklara erişmek için oturum açmak gerekebilir.                                                                      |
| [Destek blog](http://aka.ms/AXSupportBlog)                              | Dynamics 365 for Operations Destek ekibi tarafından yayınlanan ipuçlarını ve püf noktaları sağlar.                                                                                                                                                  |
| [MSDN](http://aka.ms/AXMSDN)                                             | Geliştiriciler için yazılmış önceki sürümlerin içeriklerini barındırır.                                                                                                                                                                       |
| [TechNet](http://aka.ms/TechNet)                                         | BT uzmanları ve uygulama kullanıcıları için yazılmış önceki sürümlerdeki içeriği barındırır.                                                                                                                                           |
| [Dynamics topluluğu](http://community.dynamics.com/en/)                  | Bloglar, forumlar ve videoları barındırır.                                                                                                                                                                                                           |
| [Microsoft.com/Dynamics/](http://www.microsoft.com/dynamics/)                 | Değerlendirme ve satış bilgileri sağlar.                                                                                                                                                                                                 |



<a name="see-also"></a>Ayrıca bkz.
--------

[Dynamics 365 işlemleri için Yardım sistemi (karşıdan yüklenebilen bir Olgu Tablosu)](https://mbs.microsoft.com/files/public/CS/AX2012R3/DynamicsAXHelpSystemFactSheet.pdf)

[İşlemler için Microsoft Dynamics 365 Görev Kaydedici](../user-interface/task-recorder.md)

[Görev kayıtlarını kullanarak belgeler veya eğitim oluşturma](../user-interface/task-recorder.md)

[Yeni veya güncelleştirilmiş görev kılavuzları (Kasım 2016)](new-task-guides-november-2016.md)<ph id="t1">
</ph>[yeni veya güncelleştirilmiş görev kılavuzları (Ağustos 2016)](new-updated-task-guides-available-august-2016.md)<ph id="t2">
</ph>[yeni veya güncelleştirilmiş görev kılavuzları (Mayıs 2016)](new-updated-task-guides-available-may-2016.md)<ph id="t3">
</ph>[yeni görev kılavuzları (Şubat 2016)](new-task-guides-available-february-2016.md)







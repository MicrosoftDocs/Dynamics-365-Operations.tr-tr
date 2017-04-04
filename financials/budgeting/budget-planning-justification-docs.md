---
title: "Bütçe planlama bloklama belgeleri"
description: "Belgeleri yaslama biçiminde anlatı belirli bir bütçeyi neden gerekli olduğunu açıklamak için bir bütçe isteyen kişiler için sağlar."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: c86d01fec3d8d7c210c7e73a034f4e9e384a0dcf
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-justification-documents"></a>Bütçe planlama bloklama belgeleri

Belgeleri yaslama biçiminde anlatı belirli bir bütçeyi neden gerekli olduğunu açıklamak için bir bütçe isteyen kişiler için sağlar. 

Bütçe planı şablonu Microsoft Word'de bütçe Yöneticisi tarafından oluşturulan ve atanan geçerli bütçe planlama işleminin. Bütçe sahipleri sonra şablonu açın ve Word içindeki otomatik olarak doldurulan veri kendi bütçe isteği doğrultusunda vardır. Daha sonra ek metin veya veri kaydetme ve bütçe planlarına kendi kişiselleştirilmiş bloklama belge iliştirme önce ekleyebilirsiniz.

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>Microsoft Dynamics Office eklenti Microsoft Word için ayarlayın.

1.  Yeni bir Microsoft Word belgesi açın.
2.  ' I **Ekle** tıklatın ve Şerit üzerindeki **deposu**.
3.  ' I tıklatın ve arama için Microsoft Dynamics Office eklenti **Ekle**.
4.  Word'de sağ bölmede **sunucu bilgileri eklemek**.
5.  Yazın veya sunucu URL'sini yapıştırın ve **Tamam**.

##### <a name="define-the-justification-template-in-microsoft-word"></a>Microsoft Word'de bloklama şablonu tanımlama

1.  ' I **tasarım** Microsoft Dynamics ofisini sonra oturum açtığınız eklenti içinde.
2.  Başlık bilgilerini kullanmak **alanlar eklemek** düğmesi.
3.  BudgetPlanJustification varlık veri kaynağını seçin ve tıklatın **İleri**. **Not:** bu varlık için herhangi bir gerekçe belge gereklidir. Diğer varlıkları kullanılabilir ancak bu varlık gelmediyse Microsoft Dynamics 365 işlemleri için geri yükleme başarısız olur.
4.  BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter ve DocumentNumber etiketler ve değerler, Word belgesine ekleyin. **Not:** gerekirse standart etiketler yerine kendi özel etiketlerinizi kullanabilirsiniz.
5.  ' I **yapılan** üstbilgi bölümünü tamamlamak için.
6.  Satır düzey ayrıntılarını bütçe planı tutarlar için ' ı **Tablo Ekle**.
7.  Yine, BudgetPlanJustification varlık veri kaynağını seçin ve'ı **İleri**.
8.  EffectiveDate, ScenarioName, AccountDisplayValue ve AccountingCurrencyExpenseAmount alanları ekleyin. **Not:** yorumlar içinde tek bir bütçe planı satırları eklemek varsa, bu burada tabloya eklenebilir.
9.  Son kullanıcıya sağlamak için tüm ek yönergeleri eklemek ve gerekli biçimlendirme veya belgenin stil gerçekleştirin.
10. Belgeyi yerel bilgisayarınıza kaydedin ve devam etmeden önce dosyayı kapatın.

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>Bloklama şablonu kullanmak için bütçe planlama işleminin ayarlamak

1.  İşlemler için Microsoft Dynamics 365 içinde gitmek **bütçeleme**&gt;**Kurulum**&gt;**bütçe planlama**&gt;**bloklama belge şablonları**.
2.  ' I **yeni** ve yeni oluşturulan Microsoft Word belgenizi gösterin.
3.  Şablon görüntü adı ve açıklama girin. Click **OK**.
4.  Git **bütçeleme**&gt;**Kurulum**&gt;**bütçe****planlama**&gt;**bütçe planlama işleminin**.
5.  Burada bloklama şablonu kullanılması gerektiğini ve'ı tıklatın işlem **düzenleme**.
6.  İçinde **bloklama belge şablonu** alanında uygun şablonu seçin ve kaydedin.

##### <a name="edit-and-save-personalized-justification-documents"></a>Düzenleme ve kişiselleştirilmiş bloklama belgeleri kaydetme

1.  Dynamics 365 işlemleri için yeni bir bütçe planı oluşturun veya varolan bir bütçe planı açın.
2.  İçinde **gerekçe** aþaðý açýlan menüsünden, select **yeni yaslama oluşturmak**.
3.  Ayrıntılar doldurduktan sonra kişiselleştirilmiş belgeyi karşıya yüklemek için seçin **gerekçe** aþaðý açýlan menü.




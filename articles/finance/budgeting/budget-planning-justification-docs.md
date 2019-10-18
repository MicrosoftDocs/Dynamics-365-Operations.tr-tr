---
title: Bütçe planlama gerekçe belgeleri
description: Gerekçe belgeleri, belirli bir bütçenin neden gerekli olduğunu açıklamak isteyenler için açıklama sağlar.
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 321da6643b421070ddd9f32bddd3e8d72f0adb86
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188568"
---
# <a name="budget-planning-justification-documents"></a>Bütçe planlama gerekçe belgeleri

[!include [banner](../includes/banner.md)]

Gerekçe belgeleri, belirli bir bütçenin neden gerekli olduğunu açıklamak isteyenler için açıklama sağlar. 

Bir bütçe planı şablonu, bütçe yöneticisi tarafından Microsoft Word içerisinde oluşturulur ve geçerli bütçe planlama işlemine atanır. Bütçe sahipleri daha sonra şablonu açabilir ve verinin bütçe isteklerine göre Word içerisinde otomatik doldurulmasını sağlayabilir. Daha sonra, kaydetmeden önce ek metin veya veri ekleyebilir ve kişiselleştirilmiş gerekçe belgelerini bütçe planına ekleyebilirler.

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a>Microsoft Word için Microsoft Dynamics Office Eklentisini ayarlayın

1.  Yeni bir Microsoft Word belgesi oluşturma.
2.  Şerit üzerinde **Ekle**'yi tıklatın ve **Depola**'yı tıklatın.
3.  Microsoft Dynamics Office Eklentisi'ni aratın ve **Ekle**'yi tıklatın.
4.  Word içerisinde, sağdaki bölmede **Sunucu bilgisi ekle**'yi tıklatın.
5.  Sunucu URL'sini yazın veya yapıştırın ve **Tamam**'ı tıklatın.

##### <a name="define-the-justification-template-in-microsoft-word"></a>Microsoft Word içinde doğrulama şablonunu tanımlayın

1.  Microsoft Dynamics Office Ekletisi'ne oturum açtıktan sonra **Tasarım**'ı tıklatın.
2.  Başlık bilgisi için **Alanlar ekle** düğmesini kullanın.
3.  BudgetPlanJustification varlık veri kaynağını seçin ve **İleri**'yi tıklatın. **Not:** Bu varlık tüm gerekçe belgeleri için gereklidir. Diğer varlıklar da kullanılabilir ancak bu varlık dahil edilmemişse Microsoft Dynamics 365 Finance'a geri yüklerken başarısız olur.
4.  BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter ve DocumentNumber etiketlerini ve değerlerini Word dosyasına ekleyin. **Not:** Gerekirse standart etiketler yerine kendi özel etiketlerinizi kullanabilirsiniz.
5.  Başlık bölümünü tamamlamak için **Tamam**'ı tıklatın.
6.  Bütçe planı tutarlarının satır düzeyi ayrıntıları için **Tablo ekle**'yi tıklatın.
7.  Daha sonra yine BudgetPlanJustification varlık veri kaynağını seçin ve **İleri**'yi tıklatın.
8.  EffectiveDate, ScenarioName, AccountDisplayValue ve AccountingCurrencyExpenseAmount için alanlar ekleyin. **Not:** Yorumlar, Tekil bütçe planı satırlarına eklenmek için kullanılabilirse, bunlar buradaki tabloya eklenebilir.
9.  Son kullanıcıya sağlamak için varsa ek yönergeleri ekleyin ve belge üzerinde gerekli biçimlendirme ve stilleri gerçekleştirin.
10. Belgeyi yerel bilgisayarınıza kaydedin ve devam etmeden önce dosyayı kapatın.

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a>Gerekçe şablonunu kullanmak için Bütçe planlama işlemini ayarlama

1.  **Bütçelendirme** &gt; **Kurulum** &gt; **Bütçe planlama** &gt; **Gerekçe belge şablonları**'na gidin.
2.  **Yeni**'yi tıklatın ve yeni oluşturulan Microsoft Word belgenize gidin.
3.  Şablon görüntüleme adı ve açıklama girin. **Tamam** seçeneğini tıklatın.
4.  **Bütçeleme** &gt; **Kurulum** &gt; **Bütçe** **planlama** &gt; **Bütçe planlama işlemi**'ne gidin.
5.  Gerekçe şablonunun kullanılacağı işlemi seçin ve **Düzenle**'yi tıklatın.
6.  **Gerekçe belge şablonu** alanında, uygun şablonu seçin ve kaydedin.

##### <a name="edit-and-save-personalized-justification-documents"></a>Kişiselleştirilmiş gerekçe belgelerini düzenleme ve kaydetme

1.  Yeni bir bütçe planı oluşturun veya var olan bir bütçe planını açın.
2.  **Gerekçe** aşağı açılan menüsünden **Yeni gerekçe oluşturma**'yı seçin.
3.  Ayrıntılar doldurduktan sonra, karşıya yüklemek için **Gerekçe** aşağı açılan menü üzerinden kişiselleştirilmiş belgeyi seçin.





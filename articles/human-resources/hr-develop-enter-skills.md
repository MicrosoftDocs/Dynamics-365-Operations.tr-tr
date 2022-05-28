---
title: Yetenekleri girin
description: Çalışanlar ve yöneticiler Dynamics 365 Human Resources'da yetenek girebilir.
author: twheeloc
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 32f08fa45c023c587d89623a12f101f50ef4a5fb
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693017"
---
# <a name="enter-skills"></a>Yetenekleri girin

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dynamics 365 Human Resources'ta çalışanlar, başvuranlar veya ilgili kişiler için hedef yetenekler veya gerçek yetenekler girebilirsiniz. Hedef yetenek, bir kişinin elde etmeyi planladığı yetenektir. Gerçek yetenek, bir kişinin sahip olduğu yetenektir.

## <a name="create-a-workflow-to-auto-approve-skills"></a>Otomatik onay becerileri için iş akışı oluştur

Onay gerektirmeden yetenekleri girmek için, otomatik onay becerileri için bir iş akışı oluşturmanız gerekir.

> [!NOTE]
> Çalışanlar tarafından girilen yetenekler her zaman yönetici onayını gerektirir. Bu iş akışı, yalnızca yöneticiler tarafından çalışanlar adına girilen yetenekleri otomatik olarak onaylar.

1. **Personel yönetimi** çalışma alanında, **Bağlantılar**'ı seçin.

2. **Kurulum**'un altında, **İnsan kaynakları iş akışlarını** seçin.

3. **Yeni**'yi seçin.

4. **İş akışı oluştur** bölmesinde, **Çalışan yetenekleri**'ni seçin.

   [![Çalışan becerileri iş akışı seçme.](media/hr-develop-skills-new-workflow.png)](media/hr-develop-skills-new-workflow.png)

5. **Bu dosyada açılsın mı?** iletişim kutusunda **Aç**'ı seçin. İstendiğinde, kimlik bilgilerinizi girin.

6. İş akışı Düzenleyicisi 'nde, **onay becerileri** iş akışı öğesini seçin ve tuvale sürükleyin.

   [![Onay yeteneklerini iş akışı öğesi seçme.](media/hr-develop-skills-element.png)](media/hr-develop-skills-element.png)

7. **Başlangıç** öğesini **onay yetenekleri 1** öğesine bağlayın ve sonra da **onay yetenekleri 1** öğesini **son** öğeye bağlayın. **Son** öğeyi görmek için aşağı doğru gitmeniz gerekebilir. Diğer öğelere daha yakın bir yere sürükleyebilirsiniz.

   [![İş akışı öğelerini bağlama.](media/hr-develop-skills-connect-elements.png)](media/hr-develop-skills-connect-elements.png)

8. **Onay yetenekleri 1** iş akışı öğesini çift tıklatın ve sonra **Adım 1** öğesini sağ tıklatın. **1. adımı** Sağ tıklatın ve sonra **Özellikler**'i seçin.

9. **Özellikler** penceresinde, sol taraftaki Gezinti çubuğunda **Koşul**'u seçin.

10. **Bu adımı yalnızca aşağıdaki koşul karşılandığında çalıştır** belirleyin.

11. **Koşulu ekle**'yi seçin. **Nerede** seçeneğinden sonra, **Çalışan Self Servis yeteneklerini** seçin ve ardından **Çalışan Self Servis becerileri**'ni seçin. **is**'den sonra, **alan** seçin ve **kişiye göre kullanıcı ilişkisi.Kişi**'yi seçin.

    [![Koşul belirtme.](media/hr-develop-skills-condition.png)](media/hr-develop-skills-condition.png)

12. Sol gezinti çubuğunda **atama** 'ı seçin.

13. **Atama türü** sekmesinde **hiyerarşi** seçin.

14. **Hiyerarşi seçimi** sekmesinde, **Hiyerarşi türü:** alanında, **Yönetim hiyerarşisi**'ni seçin.

    [![Yönetim hiyerarşisini belirtme.](media/hr-develop-skills-hierarchy.png)](media/hr-develop-skills-hierarchy.png)

15. **Kapat**'ı seçin, tuval içerik listesinde **iş akışı**'nı seçin ve sonra **Kaydet ve Kapat**'ı seçin.

İş akışları oluşturmayla ilgili daha fazla bilgi için bkz. [İş akışı sistemine genel bakış](../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md?toc=/dynamics365/human-resources/toc.json).

## <a name="enter-skills-for-a-worker"></a>Bir işçi için yetenekler girin

1. Çalışan seçin.

2. **İşçi** sayfasının eylem çubuğunda , **kişi**'yi seçin ve sonra da **yetenekler**'i seçin.

3. **Yetenekler** sayfasında, her yetenek için aşağıdaki alanları tamamlayın:

   - **Yetenek**: bir yetenek seçin.
   - **Düzey türü**: çalışanın zaten sahip olduğu bir yetenek için **gerçek** 'ı seçin veya çalışanın doğru çalıştığı bir yetenek için **hedef** seçin.
   - **Düzey**: çalışan becerisi için bir düzey seçin.
   - **Düzey tarihi**: Takvim aracında bir tarih seçin.
   - **Denetleyici** : uygunsa, listeden bir Denetleyicisi seçin. Aramanıza filtre uygulayabilirsiniz.
   - **Deneyim yılı**: deneyim yıllarına girin.
   - **Doğrulandı**: Yetenek doğrulanırsa, kutuyu işaretleyin.
   - **Doğrulayan**: Doğrulayıcı adını girin.

4. Yetenekleri girmeyi tamamladığınızda, **Kaydet**'i seçin.

## <a name="see-also"></a>Ayrıca bkz.

[Yetenekleri konfigüre et](hr-develop-skills.md)<br>
[Becerileri eşleştirme](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

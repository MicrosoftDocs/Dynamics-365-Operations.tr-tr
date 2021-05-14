---
title: İstihdamı bulunmayan çalışanlar
description: Kuruluşunuzla gelecekte, etkin veya geçmişe ait iş kaydı olmayan çalışanlar, İş kaydı olmayan çalışanlar formunda görünür.
author: andreabichsel
ms.date: 04/06/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1a137de25924f4c4ec6f6b1fe70f9d21af591c0
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924583"
---
# <a name="workers-without-employment"></a>İstihdamı bulunmayan çalışanlar

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Kuruluşunuzla gelecekte, etkin veya geçmişe ait iş kaydı olmayan çalışanlar, **İş kaydı olmayan çalışanlar** formunda görünür. Bu duruma sahip çalışanlar, iş kaydı olmayan çalışanları içe aktardığınızda veya **Çalışanlar > İş geçmişi** ile bir çalışanın gününü sildiğinizde görüntülenebilir.

Varsayılan olarak, **İş kaydı olmayan çalışanlar** formu aşağıdaki roller tarafından kullanılabilir:

- İnsan Kaynakları Yardımcısı
- İnsan Kaynakları Yöneticisi
- İşe alan
- Maaş ve Kazançlar Yöneticisi
- Bordro Yöneticisi
- Bordro Müdürü
- Eğitim Müdürü

**İş kaydı olmayan çalışanlar** listesinde, listelenen kişileri silebilirsiniz. Varsayılan olarak, bu ayrıcalık İnsan Kaynakları Yardımcısı rolüne verilir. Bu ayrıcalığı aşağıdaki adımlarla diğer rollere verebilirsiniz:

1. **Sistem yönetimi**'ni ve sonra **Güvenlik yapılandırması**'nı seçin.

2. **Ayrıcalıklar** sekmesinde , **çalışanları korumak** için **ayrıcalıklar** listesine filtre uygulayın.

   [![Ayrıcalık listesini filtreleme](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)

3. **Başvurular** sütununda, **menü öğelerini görüntüle**'yi seçin.

4. **Menü öğelerini görüntüle**'de **HcmWorkersWithoutEmployment**'ı seçin.

   [![Form seç](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)

5. **İzin vermek** için **Silme** iznini ayarlayın.

6. **Yayımlanmamış nesneler** sekmesini seçin.

7. **Tümünü yayımla**'yı seçin.

   [![Değişiklikleri yayımla](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
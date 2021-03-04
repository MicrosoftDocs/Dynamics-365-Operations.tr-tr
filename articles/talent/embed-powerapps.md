---
title: Power Apps uygulamalarını Dynamics 365 Human Resources'de katıştırma
description: Bu konu, Microsoft Power Apps menü öğesinin Sistem yönetim modülünden kaybolduğu sorunu ortadan kaldırmayı açıklamaktadır.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8275a8a7c68fa13d6b9880c4c411deaa2dcbb998
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462787"
---
# <a name="embed-power-apps-apps-in-dynamics-365-human-resources"></a>Power Apps uygulamalarını Dynamics 365 Human Resources'de katıştırma

**Çıkış**

**Power Apps** menü öğesi, **Sistem yönetimi** modülünden kayboldu.

**Nedeni**

Kullanıcı arabirimi (UI) tasarımı değiştirildi ve Microsoft Power Apps, şimdi standart kişiselleştirme modeline dahildir.

**Çözünürlük**

Power Apps'ın katıştırılma şekli değiştirildi. Artık Power Apps kişiselleştirme modeli aracılığıyla eklenir. Power Apps'i Microsoft Dynamics 365 Talent içinde neredeyse her sayfaya ekleyebilirsiniz.

Talent içerisinde Power Apps'in nasıl katıştırılacağı hakkında bilgi için bkz. [Power Apps'i katıştırma](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps).

Değişimden önce uygulamalarını katıştırmış olan her Power Apps kullanıcısının yeni modele yükseltilmiş olması gerekir.

**Power Apps** düğmesi, Talent içindeki neredeyse her sayfanın sağ üst kösesindedir. Uygulamaları eklemek için bu düğmeyi kullanın.

Aşağıda bir örnek verilmiştir.

1. **Personel yönetimi \> Bağlantılar \> Çalışanlar \> Personel**.
2. **Power Apps** düğmesini ve ardından **Power Apps'ten uygulama ekle**'yi seçin.

    ![Power Apps düğmesi](media/png.png)

3. **Power Apps'ten uygulama ekle** iletişim kutusundaki alanları doldurun.

    ![Power Apps'ten uygulama ekle iletişim kutusu](media/insert-powerapp.png)

Alternatif olarak bu adımları izleyin.

1. Sayfanın eylem bölmesinde, **Seçenekler** sekmesinde, **Kişiselleştir** grubunda **Bu sayfayı kişiselleştir**'i seçin.

    ![Seçenekler sekmesinde Kişiselleştir grubu](media/options.png)

    Kişiselleştirme araç çubuğu görüntülenir.

2. Araç çubuğunda, **Power Apps'tenuygulama ekle**'yi seçin.

    ![Kişiselleştirme araç çubuğunu kullanarak Power Apps'ten uygulama ekleme](media/powerapp-bar.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
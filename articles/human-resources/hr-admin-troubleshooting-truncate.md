---
title: Pozisyon hiyerarşisinde metin kesilmesini engelleme ve Visio'ya aktarma
description: Bu konuda, Microsoft Dynamics 365 Human Resources uygulamasında pozisyon hiyerarşisindeki kişilerin ve pozisyonların adlarının kısaltılması sorununun nasıl düzeltileceği açıklanmaktadır.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 20331b3a06301d10177fd0d5734f6e33994ef123
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693962"
---
# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a>Pozisyon hiyerarşisinde metin kesilmesini engelleme ve Visio'ya aktarma


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Stok çıkışı**

Bir müşteri, Microsoft Dynamics 365 Human Resources içinde konum hiyerarşisini görüntülerse, bireylerin ve pozisyonların adları kesilir. Bu nedenle, bir ekran görüntüsü almak veya hiyerarşiyi yazdırıp dağıtmak zor olabilir.

![Pozisyon hiyerarşisi.](media/position-h.png)

**Nedeni**

Bu davranış tasarımdan kaynaklanır.

**Çözüm**

Ne yazık ki, kullanıcılar kolayca metin boyutunu değiştiremezler. Ancak, konum hiyerarşisini İnsan Kaynakları'nın dışına aktarabilir ve daha sonra Microsoft Visio'ya içe aktarabilirsiniz. Aşağıdaki makale Microsoft Dynamics AX 2012 için yazılmıştır, ancak prosedür halen İnsan Kaynakları için geçerlidir: [Microsoft Visio'ya bir konum hiyerarşisi dışa aktarmak](/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).

Visio'ya dışa aktarmak için aşağıdaki adımları izleyin.

1. İnsan Kaynakları, **pozisyon** listesi sayfasını açın.

    Kuruluş yapısı diyagramına daha fazla bilgi eklemek için **Pozisyonlar** listesine alanlar ekleyin, böylece bu yordamın ileri bölümündeki **Kuruluş şeması sihirbazı**'nı kullandığınızda bu alanlar kullanılabilir hale gelir.

2. Eylem Panosu üzerinde **Microsoft Office içinde aç** düğmesini seçin ve sonra **Excel'e dışa aktar** altında, **Konumlar**'ı seçin. Bunun yerine, Ctrl+T tuşlarına basın.

    ![Konumlar listesi sayfasını Excel'e dışa aktarın.](media/org-admin.png)

3. Dışa aktarılan Excel dosyasını kaydedin.

    ![Excel iletişim kutusuna aktarma.](media/export-excel.png)

4. Visio içinde **Visio - Yeni oluştur** öğesini seçin ve **İş** şablon kategorisini seçin.

    ![Yeni diyagram.](media/new.png)

5. **Kuruluş Şeması Sihirbazı**'nı seçin ve sonra **Oluştur**'u seçin.

    ![Kuruluş Şeması Sihirbazı iletişim kutusu.](media/orgchart-wizard.png)

6. **Halihazırda bir dosya veya veri tabanında depolanmış olan bilgi**'yi seçin ve sonra **İleri**'yi seçin.

    ![Kuruluş Şeması Sihirbazı 1.](media/orgchart-wizard7.png)

7. **Bir metin, Org Plus (\*.txt), veya Excel dosyası** öğesini seçin ve sonra **İleri**'yi seçin.

    ![Kuruluş şeması sihirbazı 2.](media/orgchart-wizard3.png)

8. Konum hiyerarşisini içeren seçilen dışa aktarılan Excel dosyasını seçmek için tarayın ve sonra **İleri**'yi seçin.

    ![Kuruluş Şeması Sihirbazı 3.](media/orgchart-wizard2.png)

9. **Adı** alanında **Konum** olarak ayarlayın, **Raporlar için** alanını **Konuma raporlar** olarak ayarlayın ve sonra **İleri**'yi seçin.

    ![Kuruluş Şeması Sihirbazı 4.](media/orgchart-wizard1.png)

10. Her bir düğümde gösterilecek alanları seçin ve sonra **İleri**'yi seçin.

    ![Kuruluş Şeması Sihirbazı 5.](media/orgchart-wizard5.png)

11. **Konum** sütununu **Veri alanlarını şekillendir** listesine ekleyin ve sonra **İleri**'yi seçin.

    ![Kuruluş Şeması Sihirbazı 6.](media/orgchart-wizard6.png)

12. Resimler şu anda kullanılamıyor. Bu nedenle, bir sonraki sayfada **İleri**'yi seçin.
13. **Sihirbazın kuruluş şemamı sayfalar arasında otomatik olarak kesmesini istiyorum**'u seçin.

    ![Kuruluş Şeması Sihirbazı 7.](media/orgchart-wizard4.png)

14. **Bitir**'i seçin.

    Yapı içerisinde bulunmayan herhangi bir konum varsa, onları diyagrama eklemeniz istenir.

Visio içinde oluşturulan diyagram, her bir yöneticiyi farklı bir çalışma sayfasında gösterir.

Diyagrama dahil etmeyi seçtiğiniz alanlara dayalı olarak, her bir düğüm Visio dosyası oluşturulduğunda uygun bilgiyi gösterir.

![Hiyerarşi diyagramı.](media/hierarchy.png)

**Ek seçenek**

İnsan Kaynakları içerisinde, **Kişiler** çalışma alanını hiyerarşiye dayalı bazı bilgileri görmek için kullanabilirsiniz.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: "Konum hiyerarşisi üzerinde metin kesmeden kaçının ve Visio'ya dışa aktarın"
description: "Bu konu adlarını ve pozisyonları kişiler müşteriler yetenek için Microsoft Dynamics 365 for Talent için hiyerarşi görüntülediğinizde nerede kesiliyor sorununu açıklar. Metin kesme, hiyerarşinin ekran görüntüsünün veya baskısının alınmasını zorlaştırabilir."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: b688a396e3b384aedb06c470b1634150ae7aa038
ms.contentlocale: tr-tr
ms.lasthandoff: 12/04/2018

---

# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a>Konum hiyerarşisi üzerinde metin kesmeden kaçının ve Visio'ya dışa aktarın

[!include [banner](includes/banner.md)]

**Stok çıkışı**

Bir müşteri, Microsoft Dynamics 365 for Talent içinde konum hiyerarşisini görüntülerse, bireylerin ve pozisyonların adları kesilir. Bu nedenle, bir ekran görüntüsü almak veya hiyerarşiyi yazdırıp dağıtmak zor olabilir.

![Pozisyon hiyerarşisi](media/position-h.png)

**Nedeni**

Bu davranış tasarımdan kaynaklanır.

**Çözünürlük**

Ne yazık ki, kullanıcılar kolayca metin boyutunu değiştiremezler. Ancak, konum hiyerarşisini Talent'in dışına aktarabilir ve daha sonra Microsoft Visio'ya içe aktarabilirsiniz. Aşağıdaki makale Microsoft Dynamics AX 2012 için yazılmıştır, ancak prosedür halen Talent için geçerlidir: [Microsoft Visio'ya bir konum hiyerarşisi dışa aktarmak](https://docs.microsoft.com/en-us/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio).

Visio'ya dışa aktarmak için aşağıdaki adımları izleyin.

1. Talent içerisinde **Konumlar** liste sayfasını açın.

    Kuruluş yapısı diyagramına daha fazla bilgi eklemek için **Konumlar** listesine alanlar ekleyin, böylece bu prosedürdeki sihirbazı kullandığınızda kullanılabilir olurlar.

2. Eylem Panosu üzerinde **Microsoft Office içinde aç** düğmesini seçin ve sonra **Excel'e dışa aktar** altında, **Konumlar**'ı seçin. Bunun yerine, Ctrl+T tuşlarına basın.

    ![Konumlar listesi sayfasını Excel'e dışa aktarın](media/org-admin.png)

3. Dışa aktarılan Excel dosyasını kaydedin.

    ![Excel iletişim kutusuna dışa aktarmak](media/export-excel.png)

4. Visio içinde **Visio - Yeni oluştur** öğesini seçin ve **İş** şablon kategorisini seçin.

    ![Yeni diyagram](media/new.png)

5. **Kuruluş Şeması Sihirbazı**'nı seçin ve sonra **Oluştur**'u seçin.

    ![Kuruluş Şeması Sihirbazı iletişim kutusu](media/orgchart-wizard.png)

6. **Halihazırda bir dosya veya veri tabanında depolanmış olan bilgi**'yi seçin ve sonra **İleri**'yi seçin.

    ![Kuruluş Şeması Sihirbazı 1](media/orgchart-wizard7.png)

7. **Bir metin, Org Plus (\*.txt), veya Excel dosyası** öğesini seçin ve sonra **İleri**'yi seçin.

    ![Kuruluş şeması sihirbazı 2](media/orgchart-wizard3.png)

8. Konum hiyerarşisini içeren seçilen dışa aktarılan Excel dosyasını seçmek için tarayın ve sonra **İleri**'yi seçin.

    ![Kuruluş Şeması Sihirbazı 3](media/orgchart-wizard2.png)

9. **Adı** alanında **Konum** olarak ayarlayın, **Raporlar için** alanını **Konuma raporlar** olarak ayarlayın ve sonra **İleri**'yi seçin.

    ![Kuruluş Şeması Sihirbazı 4](media/orgchart-wizard1.png)

10. Her bir düğümde gösterilecek alanları seçin ve sonra **İleri**'yi seçin.

    ![Kuruluş Şeması Sihirbazı 5](media/orgchart-wizard5.png)

11. **Konum** sütununu **Veri alanlarını şekillendir** listesine ekleyin ve sonra **İleri**'yi seçin.

    ![Kuruluş Şeması Sihirbazı 6](media/orgchart-wizard6.png)

12. Resimler şu anda kullanılamıyor. Bu nedenle, bir sonraki sayfada **İleri**'yi seçin.
13. **Sihirbazın kuruluş şemamı sayfalar arasında otomatik olarak kesmesini istiyorum**'u seçin.

    ![Kuruluş Şeması Sihirbazı 7](media/orgchart-wizard4.png)

14. **Bitir**'i seçin.

    Yapı içerisinde bulunmayan herhangi bir konum varsa, onları diyagrama eklemeniz istenir.

Visio içinde oluşturulan diyagram, her bir yöneticiyi farklı bir çalışma sayfasında gösterir.

Diyagrama dahil etmeyi seçtiğiniz alanlara dayalı olarak, her bir düğüm Visio dosyası oluşturulduğunda uygun bilgiyi gösterir.

![Hiyerarşi diyagramı](media/hierarchy.png)

**Ek seçenek**

Talen içerisinde, **Kişiler** çalışma alanını hiyerarşiye dayalı bazı bilgileri görmek için kullanabilirsiniz.


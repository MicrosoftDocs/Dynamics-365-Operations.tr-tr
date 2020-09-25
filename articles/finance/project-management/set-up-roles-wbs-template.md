---
title: İş kırılım yapısı şablonlarında rolleri ayarlama
description: Bu konu, iş kırılım yapısı şablonları ile ilgili rol bilgilerini ayarlama hakkında bilgi sağlar.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5dfb429eae933ba4d687ec4cbd417d2f78308e47
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760686"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>İş kırılım yapısı şablonlarında rolleri ayarlama

[!include [banner](../includes/banner.md)]

Proje yöneticileri, yeni projeler için İş Kırılım Yapısı (İKY) oluştururken uygulayabilecekleri İKY şablonlarını ayarlayabilirler. Proje yöneticileri bir şablon oluştururken roller ekleyebilirler. WBS şablonuna rol atamak için aşağıdaki yordamı kullanın. 

1. **Proje yönetimi ve muhasebe** > **Kurulum** > **Projeler** > **İş kırılım yapısı şablonları**'nı seçin.
2. Seçilen İKY şablonu için **Ayrıntıları**'nı seçin.
3. Listeden bir görev seçin ve **Rol** alanında, göreve atamak için bir rol seçin.

## <a name="work-with-a-wbs"></a>İKY ile çalışma

Yeni bir İKY oluşturabilir veya mevcut bir İKY şablonundan İKY kopyalayabilirsiniz. Proje Yöneticisi, İKY'deki yeni görevlere roller atayarak kaynakları kolayca yönetebilir. Roller, bir kaynak edinildikten veya görevde çalışmak üzere onaylı bir kaynak tanımlandıktan sonra değiştirilebilir. Bu esneklik, proje yöneticilerinin aşağıdaki görevleri gerçekleştirmesine olanak sağlar:

- İKY iş paketleri için gereken kaynak sayısını belirlemek.
- Proje maliyetlerini tahmin etmek.
- Ön bütçe belirlemek.
- Roller ve kaynakları temel alarak faaliyet süresini tahmin etmek.
- Kullanılabilir proje bilgilerine dayanarak bazı proje yönetim planları geliştirmek.

Kaynak oluşturma işlevinin daha etkin kullanılması için İKY'ye ek seçenekler eklenmiştir.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Seçenek</th>
<th>Açıklama</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kaynak atamaları</td>
<td>İKY'deki görevler için atanan kaynakları, tarihleri, saat sayısını ve rezervasyon türünü görüntüleyin.</td>
</tr>
<tr class="even">
<td>Takımı otomatik olarak oluştur</td>
<td>Görevle ilişkili rolleri kullanarak planlanmış kaynakları otomatik olarak ekleyin. Finance, rollere göre çok ölçütlü karar analizini kullanarak planlanmış kaynakları otomatik olarak önerir. İKY'deki görevler için roller ve çalışma (saat) ayarlandıktan ve yapı serbest bırakıldıktan sonra, <strong>Ekibi otomatik oluştur</strong>'u seçin. Gereken sayıda planlanmış kaynak İKY'ye ve <strong>Proje ve ekip planlama</strong> sekmesine eklenir.</td>
</tr>
<tr class="odd">
<td>Kaynak (açılan liste)</td>
<td><strong>Kaynak atamayı başlat </strong>sayfasında, belirtilen süreye göre kesin rezervasyon veya geçici rezervasyon yapmak için kaynakları seçebilirsiniz. Kaynak faaliyetlerini görmek ve süresini ayarlamak için görüntüleme ayarlarını düzenleyebilirsiniz. Aşağıdaki seçenekleri kullanarak, kaynakları seçebilir ve iş paketi düzeyinde atayabilirsiniz:
<ul>
<li><strong>Kabul et</strong> – Bir göreve atanan kaynakla ilgili değişiklikleri onaylar.</li>
<li><strong>İptal et</strong> – Bir göreve atanan kaynakla ilgili değişiklikleri iptal eder.</li>
<li><strong>Otomatik olarak ata</strong> – Kullanılabilir, eşleşen bir role sahip bir personelli kaynak otomatik olarak seçilir ve seçilen göreve atanır.</li>
</ul></td>
</tr>
</tbody>
</table>

1. **Tüm projeler** sayfasında, **XYZ Yükseltme Aşaması 2** projesini seçin.
2. **Plan** > **Etkinlikler** > **İş kırılım yapısı**'nı seçin.
3. İKY'ye aşağıdaki düzey bir faaliyetlerini eklemek için **Yeni**'yi seçin:

    - Başlatma
    - Planlama
    - Yürütme
    - İzleme ve Denetim
    - Kapalı

4. Aşağıda gösterildiği gibi tarihleri ve çabayı (saatler) girin.

    [![Tarih ve çabayı ayarlama](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. **Başlatma** görev satırını seçin, ardından **Rol** alanında **Kıdemli Proje Yöneticisi**'ni seçin.
6. **Yayımla**'yı seçin.
7. Aynı satırda, **Kaynak** alanında **Daniel Goldschmidt**'i seçin ve sonra **Uygula**'yı seçin.
8. **Planlama** görev satırını seçin ve ardından **Rol** alanında **İş analisti**'ni seçin.
9. **Yayımla**'yı seçin ve ardından **Ekibi otomatik oluştur**'u seçin.
10. Görüntülenen mesaj kutusunda **Evet**'i seçin.
11. **Kaynak** alanında, değerin **İş analisti 1** olduğunu doğrulayın.
12. **İş analisti 1** kaynağı için aramayı açın ve **Kaynak atamalarını aç**'ı seçin. Daha sonra görev için bir çalışan seçin.
13. **Geçici atama** &gt; **Tam kapasite**'yi seçin.

    > [!NOTE] 
    > Kaynakların sayısı 1'de kaldığı için belirtilen kaynağın artık 2 olduğunu belirten bir uyarı almazsınız.

14. **İş kırılım yapısı** sayfasında, İKY'deki kaynak atamasını doğrulayın ve **Kaydet**'i seçin.

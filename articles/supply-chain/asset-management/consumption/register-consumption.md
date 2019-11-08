---
title: Tüketimi kaydetme
description: Bu konuda Varlık Yönetimi'nde tüketimi kaydetme işlemi açıklanmaktadır.
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 43f14a1cbd016335b857fdff1147740b27d5c765
ms.sourcegitcommit: 0099fb24f5f40ff442020b488ef4171836c35c48
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/23/2019
ms.locfileid: "2653335"
---
# <a name="register-consumption"></a>Tüketimi kaydetme

[!include [banner](../../includes/banner.md)]

 

Bir iş emrinde bakım işi tamamlandığında, bir sonraki adım tüketim kayıtları yapmak ve günlükleri deftere nakletmektir. Aşağıdaki tüketim türlerinde kayıt yapabilirsiniz: Saatler, maddeler ve giderler. Farklı tüketim türleri **İş emri günlükleri** sayfasında kaydedilir ve deftere nakledilir. **Varlık Yönetimindeki** günlük kurulumu **Proje yönetimi ve muhasebe** modülündeki saatler, maddeler ve giderlere ilişkin ayrı günlükler oluşturmak ve deftere nakletmek amacıyla kullanılır.

Bazı durumlarda, bir iş emrine tahmin satırları ekleyebilir veya silebilirsiniz. Bir iş emri yaşam döngüsü durumu, ilgili proje türü ve proje tipiyle ilgili aşama kuralları kurulumu, günlük satırları ekleyip ekleyemeyeceğinizi veya düzenleyip düzenleyemeyeceğinizi belirler. [Proje yönetimi ve muhasebe tümleştirmesinde](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md) iş emri yaşam döngüsü durumları ve ilgili proje aşamaları hakkında daha fazla bilgi edinin.

>[!NOTE]
>Bir iş emri yaşam döngüsü durumunda günlüklerin otomatik olarak deftere nakledilmesini ayarlamak mümkündür. Daha fazla bilgi için bkz. [İş emri yaşam döngüsü durumları](../setup-for-work-orders/work-order-lifecycle-states.md).

1. **Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ne tıklayın.

2. İş emrini seçin ve **Günlükler**'e tıklayın.

3. İş emrine bağlı olabilecek tahmin satırlarını transfer etmek için **Tahminden kopyala**'ya tıklatın. Transfer etmek istediğiniz tüketim tiplerini seçebilirsiniz.

4. Gerekirse, **Satır ekle**'ye tıklayıp ve satırda verileri doldurarak ilgili hızlı sekmeye başka tüketim satırları da ekleyebilirsiniz.

5. Deftere nakletmeden önce günlük satırlarını doğrulamak için **Günlükleri doğrula**'yı tıklatın.

6. Günlük satırlarını deftere nakletmek için **Günlükleri deftere naklet** öğesini tıklatın.

7. Tüketim günlüklerini deftere naklettikten sonra, iş emri yaşam döngüsü durumunu güncelleştirebilirsiniz. Örneğin, iş emrinin tamamlandığını belirtmek için, yaşam döngüsü durumunu "Sona erdi" olarak güncelleştirebilirsiniz.

    - **İş emri günlükleri** sayfasının en üstündeki **Göster** alanında, hangi günlük satırlarını görmek istediğinizi seçin: **tümü**, **deftere nakledilmemiş** veya **deftere nakledilmiş**. Deftere nakledilen günlüklerin **Deftere nakledildi** onay kutusunda onay işareti vardır.  
    - İş emri günlüğünde madde satırları oluşturulduğunda, maddeyle ilgili ürün boyutları ve izleme boyutları otomatik olarak günlük satırına transfer edilir.  

Aşağıdaki ekran görüntüsü, **İş emri günlüklerindeki** bir iş emrindeki bir saat ve madde kaydı örneğini gösterir.

![Şekil 1](media/01-consumption.png)


## <a name="split-hours-on-work-orders-with-several-work-order-jobs"></a>Birkaç iş emri işine sahip iş emirlerindeki saatleri bölme

Bir iş emri birkaç iş emri işi içeriyorsa, iş saatlerini **Saatleri böl** işlevini kullanarak kaydedebilirsiniz, böylece her bir saat kayıt satırı her iş emri işinde eşit şekilde dağıtılabilir.

1. **Varlık yönetimi** > **Genel** > **İş emirleri** > **Tüm İş emirleri** veya **Etkin iş emirleri**'ne tıklayın.

2. İş emrini seçin ve **Günlükler**'e tıklayın.

3. Bölmek istediğiniz saat kayıt satırını seçin ve **Saatleri böl**'e tıklatın.

4. **İş emri bakım işlerinde saatleri böl** iletişim kutusunda oturum açan çalışanın adı otomatik olarak **Çalışan** alanında gösterilir. Gerekirse başka bir çalışan seçebilirsiniz.

5. **Kategori** alanında saat kaydı için bir kategori seçin.

6. **Saatler** alanına bölünecek çalışma saatleri sayısını ekleyin.

    ![Şekil 2](media/02-consumption.png)

7. **Tamam**'a tıklayın.

*Örnek:* Aşağıdaki ekran görüntüsünde, üç iş emri işi içeren bir iş emrine ait günlük satırları gösterilir. Üç iş saati içeren ilk satır bölünmüştür ve her bir iş emri işine bir saat kaydedilir. Üç saat kayıt satırı oluşturulduktan sonra, orijinal saat kayıt satırı (örnekteki ilk satır) ile ne yapılacağına karar verirsiniz. Olduğu gibi tutabilir veya silebilirsiniz. 

![Şekil 3](media/03-consumption.png)

## <a name="financial-dimensions-on-consumption-registrations"></a>Tüketim kayıtlarında mali boyutlar

Tüketim kayıtları yaptığınızda, farklı kayıt türleriyle ilgili mali boyutlar belirli bir dizideki kayıtlara eklenir. 

- *Saat ve Gider kayıtları:* Önce, varsa günlük başlığındaki mali boyutlar eklenir. Sonra ilgili iş emri projesindeki mali boyutlar eklenir. Son olarak, kaynaktaki (çalışan) mali boyutlar eklenir.

- *Madde kayıtları:* Önce, varsa günlük başlığındaki mali boyutlar eklenir. Ardından ilgili iş emri projesindeki mali boyutlar eklenir. Bundan sonra, tesisteki mali boyutlar eklenir. Son olarak, maddedeki mali boyutlar eklenir.

>[!NOTE]
>Üç kayıt türü için, mali boyut birleşimi doğrulanır ve geçersiz birleşimler boş bırakılır. Bu, diğer Finance and Operations uygulamalarıyla standart bir kurulumdır.


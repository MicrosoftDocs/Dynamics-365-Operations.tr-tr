---
title: Proje tahminini eleme
description: Bu konu, tamamlandıktan sonra projenin tahmini kaldırılması hakkında bilgi sağlar.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: eb323bdeb2a4701cdc9383b8da29e05a4cab107c
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410274"
---
# <a name="eliminate-a-project-estimate"></a>Proje tahminini eleme

[!include [banner](../includes/banner.md)]

Proje tahminleri, proje için tahmin edilen ve planlanan iş için mali görünüm sağlar. Bir proje için tahminlerle tanışmak için, projeyi tahmin projesine eklemelisiniz. Tahmin projesi her zaman varolan bir projeye dayalıdır, ancak birden çok proje tek bir tahmin projesine başvuruda bulunabilir. Yalnızca sabit fiyatlı ve yatırım projeleri tahmin projelerine bağlanabilir ve bu projeler tahmin kapsamındaki projeyle aynı proje grubuna ait olmalıdır.

Tahmin kapsamındaki bir projeyi elemek için, bu projenin tamamlanmış olması gerekir. Aşağıdaki adımlarda bir tahmini nasıl ortadan kaldıracağınız açıklanmaktadır.

1. **Proje yönetimi ve muhasebe** > **Tüm projeler**'e gidin ve projeyi açın. 
2. **Yönet** sekmesinde **tahminler** 'i seçin ve **tahmin** sayfasında, **yok et**'i seçin.
3. **Genel** sekmesindeki **tahmini kaldırma** sayfasında , aşağıdaki seçenekleri ayarlayın:

   - **Dönem kodu**: Uygun tahmin projeleri seçmek için kullanılacak dönem kodunu belirleyin. 
   - **Tahmin tarihi**: Eleme için uygun tahmin tarihini seçin.
   - **Süren iş uyarılarını kaldırın**: Süren iş (WIP) ile ilişkilendirilmiş bir tahmin elendiğinde bildirim sağlamak için bu seçeneği etkinleştirin. Bu seçenek etkin olmadığında, tahmin edilemeyen hareketler varsa eleme devam edemez. 
   > [!NOTE]
   > Bu seçenek yalnızca tahmin projesine eleme uygulandığında kullanılabilir. Periyodik deftere nakilleri kullanıyorsanız bu kullanılamaz. Bu ayar , **proje parametreleri** sayfasındaki **tahmin** sekmesinde yer alan ve **tahmin edilmemiş hareketlerin bulunduğu sırada eleme izni**olan ayarlar ile çalışır.
   - **Aşamayı tamamlandı olarak ayarla**: eliminasyon çalıştırıldıktan sonra tahmin projesinin aşamasını **tamamlandı** olarak ayarlamak için bu seçeneği etkinleştirin.
   - **Tahmin listesini yazdır**: Tahmin proje listesi yazılacağı zaman dahil edilecek bilgileri seçin.
   - **Bilgi Günlüğünü Göster**: Bu seçeneğin bilgi günlüğünü görüntülemesi için etkinleştirin.
   - **Deftere nakil tarihi**: tahminin genel muhasebe deftere nakil tarihini seçin.

4.  **Tamam**'ı seçin.
5. Eliminasyon işlemi tamamlandıktan sonra, elenen tahmin projesi negatif bir değerle görüntülenir. 

Bir tahmini elemeyi düşünmüyorsanız, elenen tahmini seçin ve **eleme işlemini tersine çevir** 'i seçebilirsiniz.   
